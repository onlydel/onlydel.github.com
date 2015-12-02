---
layout: page
title: Programming log
permalink: /plog/
---

### Nov 17, 2015
* ASP.NET 5에는 [common DI(Dependency Injection) 인터페이스](https://github.com/aspnet/DependencyInjection)가 만들어져 있고, 추가 라이브러리도 있는데, 
    - [https://github.com/structuremap/structuremap.dnx](https://github.com/structuremap/structuremap.dnx)
    - [http://autofac.org/](http://autofac.org/) - 공장모양 로고가 깬다.
* 토비의 스프링 3.1 에서 IoC와 DI관련 내용을 다시 읽고 있다. DI에 대해 혼자 고민하고 삽질하면서 만든 구조 덕분인지 처음 보다 훨씬 이해하기 쉬웠다. 이해하기 쉽다기 보다는 몸에 와 닫는다는 표현이 적절하다. 책은 java로 구현하고 있지만 내용은 framework에 구애를 받지 않는다. 역시 읽어보고, 해보고, 다시 읽어보고, 다시 해보고... 의 방법으로 공부하는게 좋다. 개발도 마찬가지다. 만들고, 테스트하고, 수정하고, 다시 테스트 하고.. 의 과정으로...
* AMD기반 requery.js를 통해 동적으로 모듈을 로드할 때 

### Nov 16, 2015
* 3일동안 씨름하던 오류의 원인을 찾았다. 생각지도 못했던 곳에서 원인을 찾았고 이 문제를 해결하기 위해 많은 새로운 사실을 알게 되었다.
    - 아래 오류를 만났을때 처음엔 CORS설정에 문제가 있는 것으로 생각하고 Web API쪽 ICorsPolicyProvider를 상속받아 구현한 Attribute만 계속 쭈물딱 거리고 있었다. 구글링을 해도, StackOverfllow에서도 cors로 접근할때 어떤 문제가 있는건지 찾아다녔다.
        <pre>
        XMLHttpRequest cannot load http://winlocal:49238/api/licenses. 
        The 'Access-Control-Allow-Origin' <mark>header contains multiple values</mark> 'http://examples.onlydel.dev, http://examples.onlydel.dev', but only one is allowed. 
        Origin 'http://examples.onlydel.dev' is therefore not allowed access.</pre>
    - 알고 보니 지금 서버 사이드 구성은 ASP.NET Web API + Web Sites를 붙여서 서비스 하고 있는데, Site쪽과 Web API쪽 config에 모두 cors 설정을 해두어 Response header에 Origin정보가 두개씩 붙어서 나가게 되어 사실은 Request쪽 서버에서 이를 허용해 주지 않으면 오류가 발생하는 것이었다. 마킹된 부분을 좀더 세심하게 확인했어야 하는데, 오류메시지 하나하나에 세심하게 주의를 기울여야하는데 여전히 고쳐지지 않는다.
* 도움말이던, 메뉴얼이던, 책이던 한 번에 모든 내용을 이해하기는 어렵다. 처음볼때 이해해와 두번째 볼때 이해도가 다르다. 세번정도 보면 어느정도 이해가 되는것 같다.

### Nov 14, 2015
* XECON 2015에 참석 했다.
    - PHP는 알지도 못하면서, XE가 뭔지도 모르면서 AWS와 Git과 React.js에 대한 정보를 얻고자 다녀왔다.
    - 어떤 컨퍼런스나 밋업이 도움 안되는 경우는 없는것 같다. 새로운 경험과 동기부여를 위해서는 오프라인 참여가 꼭 필요하다.

### Nov 10, 2015
* npm 을 통해 github에 있는 application 들을 실행 하는 방법에 대해 알게 되었다.
    - package.js파일에 dependency들은 $ npm install로 일괄 설치가 가능하다.
    - gulp나 grunt로 빌드 및 실행까지 일괄로 처리가 가능하다.
* AWS에서 elastic beanstalk 서비스를 통해 웹 서비스 배포 관련 방법을 알게 되었다.
    - 이재홍님의 블로그에서 도움을 받았다. [http://pyrasis.com/aws.html](http://pyrasis.com/aws.html)
    - [http://testbed.elasticbeanstalk.com](http://testbed.elasticbeanstalk.com) (무료사용계정 시간조정을 위해 접속안될 수 있음.)
