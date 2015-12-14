---
layout: post
title: ASP.NET Accounts Management
date:   2015-03-26 21:13:31 +9:00 GMT
categories: 
  - ASP.NET
  - draft
tags: 
  - ASP.NET 5
  - Identity
  - Account
---

### 들어가며

업무용 웹 애플리케이션 개발에서 사용자관리(Accounts Management)는 중요한 개발요소중 하나 입니다. ASP.NET에서 사용자관리에 대한 강좌를 하나 번역하면서 공부해 보도록 하겠습니다.

### Web API Authentication & Authorization



### CORS

Web API를 통해 Restful 서비스를 구현하면서 또 신경써야 할 부분중 하나 가 CORS(Cross-origin resource sharing)인것 같다. api서버와 application서버가 동일한 도메인에서 서비스 되면 별 문제 없겠지만, 다른 도메인에 있는 api를 호출할 경우 CORS를 고민해야 한다.(어떻게 표현해야 좋을지)

[asp.net 사이트 참조](http://www.asp.net/web-api/overview/security/enabling-cross-origin-requests-in-web-api#enable-cors)
##### AuthorizeAttribute를 이용하는 방법

AuthorizeAttribute를 override해서 cors origin이 특정 도메인인 경우 GenericPrincipal()로 가상의 인증정보를 만드는 방법이 있다. 잘 동작 하는것 같지만 사실은 cors와 인증을 구분하지 못하는 문제가 발생 하게 된다. 좋은 방법이 아니다.

<pre class="prettyprint">
using System;
using System.Collections.Generic;
using System.Linq;
using System.Security.Principal;
using System.Web;
using System.Web.Http;
using System.Web.Http.Controllers;

namespace Basecamp.Api
{
    /// <summary>
    /// 임시권한처리를 위한 attribute
    /// api를 요청한 사이트의 호스트명을 조사해서 접근권한을 부여한다.
    /// </summary>
    public class TempAuthorizationFilterAttribute : AuthorizeAttribute
    {
        /// <summary>
        /// callback
        /// </summary>
        /// <param name="actionContext"></param>
        /// <returns></returns>
        protected override bool IsAuthorized(HttpActionContext actionContext)
        {
            Uri url = HttpContext.Current.Request.Url;
            // api를 호출한 original address를 가져온다.
            Uri origin = HttpContext.Current.Request.UrlReferrer;

            //15/11/13 현재 인증체크를 위해 컨트롤러 위에다가 Authorize attribute를 추가하더라도 GenericPrincipal을
            //만들어서 RequestContext에 포함하기 때문에 로그인 한것 같은 효과를 보게 된다.
            //이런 방법으로 처리하면 안되겠다..
            if ( origin != null && (origin.Host == "basecamp.wrw.kr" ||
                                    origin.Host == "dev.basecamp.wrw.kr" ||
                                    origin.Host == "www.realgrid.com" ||
                                    // 맵북 로컬 개발용 도메인
                                    //origin.Host == "examples.onlydel.dev" ||
                                    origin.Host == "dev.www.realgrid.com" ||
                                    origin.Host == "www.realgrid.net" ||
                                    (origin.Host == "localhost" && origin.Port == 49238) ||
                                    (origin.Host == "winlocal" && origin.Port == 49238) ||
                                    (origin.Host == "localhost" && origin.Port == 63111)
                                    ) 
                )
            {
                //role은 아직 관계 없으니 빼도되지만 일단 추가한다.
                actionContext.RequestContext.Principal = 
                    new GenericPrincipal(new GenericIdentity("tempUser"), new string[] { "admin" });
            }

            //본인 호출 경로
            if (url != null && (url.Host == "localhost" && url.Port == 55256))
            {
                //role은 아직 관계 없으니 빼도되지만 일단 추가한다.
                actionContext.RequestContext.Principal =
                    new GenericPrincipal(new GenericIdentity("debugUser"), new string[] { "admin" });
            }

            return base.IsAuthorized(actionContext);
        }
    }
}
</pre>


##### EnableCors attribute


그래도 안되는데...

인터넷에는 이런 코드를 추가하라는 내용의 답변이 있는데 이것도....

<pre>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;configuration&gt;
  &lt;system.webServer&gt;
    &lt;httpProtocol&gt;
     &lt;customHeaders&gt;
       &lt;add name=&quot;Access-Control-Allow-Origin&quot; value=&quot;*&quot; /&gt;
       &lt;add name=&quot;Access-Control-Allow-Methods&quot; value=&quot;GET, POST, PUT, DELETE, OPTIONS&quot; /&gt;
     &lt;/customHeaders&gt;
    &lt;/httpProtocol&gt;
  &lt;/system.webServer&gt;
&lt;/configuration&gt;


error
XMLHttpRequest cannot load http://winlocal:49238/Token. The 'Access-Control-Allow-Origin' header contains multiple values 'http://examples.onlydel.dev, *', but only one is allowed. Origin 'http://examples.onlydel.dev' is therefore not allowed access.
</pre>
오히려 이걸 하면 /token에도 접근이 안된다.


* [Configure ASP.NET Identity with ASP.NET Web API (Accounts Management) – Part 1](http://bitoftech.net/2015/01/21/asp-net-identity-2-with-asp-net-web-api-2-accounts-management/){:target="_blank"}
* ASP.NET Identity 2.1 Accounts Confirmation, and Password/User Policy Configuration – Part 2
* Implement OAuth JSON Web Tokens Authentication in ASP.NET Web API and Identity 2.1 – Part 3
* ASP.NET Identity Role Based Authorization with ASP.NET Web API – Part 4
* ASP.NET Identity Authorization Access using Claims with ASP.NET Web API – Part 5
* AngularJS Authentication and Authorization with ASP.NET Web API and Identity – Part 6


---
**참조**

* [http://bitoftech.net/2015/01/21/asp-net-identity-2-with-asp-net-web-api-2-accounts-management/](http://bitoftech.net/2015/01/21/asp-net-identity-2-with-asp-net-web-api-2-accounts-management/){:target="_blank"}