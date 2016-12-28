---
layout: page
title: Programming log
permalink: /plog/
---

### Dec 28, 2016
* [Meteor Cookbook](http://meteorgitbook.harp.io/)

### Sep 7, 2016
* SSL무료 인증서
  * [Encrypt](https://blog.elpo.net/get-wosign-multidomain-certificate/)
* Meteor - React - Material UI Framework - [출처](https://www.facebook.com/groups/meteorschool/permalink/598472800317159/)
  * [React Material UI](http://www.material-ui.com/#/)
  * [React Grid](http://roylee0704.github.io/react-flexbox-grid/)
  * [React Responsive](https://github.com/contra/react-responsive)

### Aug 11, 2016
* hexo deploy github pages
  * [https://hexo.io/docs/deployment.html](https://hexo.io/docs/deployment.html)

### Aug 4, 2016
* mupx delpoy시 오류: 원인도 알수 없고 실제로 배포도 정상적으로 된것 같고, 실행에도 아무런 문제는 없는데 오류 메시지가 나타난다.

<pre>
nxlicensemanager/$ mupx logs --tail=50

Meteor Up: Production Quality Meteor Deployments
------------------------------------------------
Configuration file : mup.json
Settings file      : settings.json

[52.78.34.170]
> meteor-dev-bundle@0.0.0 install /bundle/bundle/programs/server
> node npm-rebuild.js
[52.78.34.170]

> bcrypt@0.8.7 install /bundle/bundle/programs/server/npm/node_modules/meteor/npm-bcrypt/node_modules/bcrypt
> node-gyp rebuild

make: Entering directory '/bundle/bundle/programs/server/npm/node_modules/meteor/npm-bcrypt/node_modules/bcrypt/build'
  CXX(target) Release/obj.target/bcrypt_lib/src/blowfish.o
  CXX(target) Release/obj.target/bcrypt_lib/src/bcrypt.o
  CXX(target) Release/obj.target/bcrypt_lib/src/bcrypt_node.o
  SOLINK_MODULE(target) Release/obj.target/bcrypt_lib.node
  COPY Release/bcrypt_lib.node
make: Leaving directory '/bundle/bundle/programs/server/npm/node_modules/meteor/npm-bcrypt/node_modules/bcrypt/build'
bcrypt@0.8.7 /bundle/bundle/programs/server/npm/node_modules/meteor/npm-bcrypt/node_modules/bcrypt
bindings@1.2.1 /bundle/bundle/programs/server/npm/node_modules/meteor/npm-bcrypt/node_modules/bindings
nan@2.3.5 /bundle/bundle/programs/server/npm/node_modules/meteor/npm-bcrypt/node_modules/nan
{
  "meteor-dev-bundle": "0.0.0",
  "npm": "3.10.5",
  "ares": "1.10.1-DEV",
  "http_parser": "2.5.2",
  "icu": "56.1",
  "modules": "46",
  "node": "4.4.7",
  "openssl": "1.0.2h",
  "uv": "1.8.0",
  "v8": "4.5.103.36",
  "zlib": "1.2.8"
}
=> Starting meteor app on port:80
[52.78.34.170] npm WARN meteor-dev-bundle@0.0.0 No description
npm WARN meteor-dev-bundle@0.0.0 No repository field.
npm WARN meteor-dev-bundle@0.0.0 No license field.
</pre>

* mup.json 파일에 ` "deployCheckWaitTime": 60,` 속성 시간을 60으로 늘리고나서 오류가 나타나지 않게 되었다. 지난번에도 그러더니... 원인은 몰라

### Aug 1, 2016
* 화면에서 버튼이나 에디터의 사용자 입력을 처리하기 위해 Session, ReactiveDic 등 Reactive Storate를 이용해 쉽게 동작을 데이터처리로 변환할 수 있다.
  * [Reactive Dict, Reactive Vars, and Session Variables](https://themeteorchef.com/snippets/reactive-dict-reactive-vars-and-session-variables/#tmc-session-variables)

### Jul 29, 2016
* router때문인지는 모르겠지만 크롬에서 template을 찾을수 없다는 에러가 발생하고 있다. safari에서는 잘 보이는 페이지가 크롬에서만 에러가 발생한다. [migrate from iron-router to flow-router](https://www.okgrow.com/posts/flow-router-migration-guide)
* meteor collection에서 특정필드(specific fields)만 가져오는 방법
  * mongoDB는 `find({username: "user"}, {name: 1, phone: 1})` 과 같이 직접 가져올 필드목록을 작성해 줬지만, meteor에서는 `{fields: {name: 1, phone: 1}}` 과 같이 `{fields: ..}`를 사용해야 한다.
* meteor-roles package 주요 API
  * addUsersToRoles ( users  roles  [group] )
  * createRole ( role ) String
  * deleteRole ( role )
  * getAllRoles () Cursor
  * getGroupsForUser ( user  [role] ) Array
  * getRolesForUser ( user  [group] ) Array
  * getUsersInRole ( role  [group]  [options] ) Cursor
  * removeUsersFromRoles ( users  roles  [group] )
  * setUserRoles ( users  roles  [group] )
  * userIsInRole ( user  roles  [group] ) Boolean
  * examples:
  <pre class="prettyprint">
Roles.addUsersToRoles(userId, 'admin')
Roles.addUsersToRoles(userId, ['view-secrets'], 'example.com')
Roles.addUsersToRoles([user1, user2], ['user','editor'])
Roles.addUsersToRoles([user1, user2], ['glorious-admin', 'perform-action'], 'example.org')
Roles.addUsersToRoles(userId, 'admin', Roles.GLOBAL_GROUP)
// non-group usage
Roles.userIsInRole(user, 'admin')
Roles.userIsInRole(user, ['admin','editor'])
Roles.userIsInRole(userId, 'admin')
Roles.userIsInRole(userId, ['admin','editor'])
//
Roles.removeUsersFromRoles(users.bob, 'admin')
Roles.removeUsersFromRoles([users.bob, users.joe], ['editor'])
Roles.removeUsersFromRoles([users.bob, users.joe], ['editor', 'user'])
Roles.removeUsersFromRoles(users.eve, ['user'], 'group1')
// per-group usage
Roles.setUserRoles(userId, 'admin')
Roles.setUserRoles(userId, ['view-secrets'], 'example.com')
Roles.setUserRoles([user1, user2], ['user','editor'])
Roles.setUserRoles([user1, user2], ['glorious-admin', 'perform-action'], 'example.org')
Roles.setUserRoles(userId, 'admin', Roles.GLOBAL_GROUP)
//
Roles.userIsInRole(user,   ['admin','editor'], 'group1')
Roles.userIsInRole(userId, ['admin','editor'], 'group1')
Roles.userIsInRole(userId, ['admin','editor'], Roles.GLOBAL_GROUP)
// this format can also be used as short-hand for Roles.GLOBAL_GROUP
Roles.userIsInRole(user, 'admin')</pre>

### Jul 28, 2016
* mongodb deploy와는 별개로 다른 문제가 생겼다. meteor를 1.4로 업데이트 하면서 mupx를 통해 deploy할 때 docker의 설정문제로 deploy가 동작하지 않는다. 그저께 즈음에[관련이슈](https://github.com/meteor/meteor/issues/7475)가 올라오긴 했지만 간단히 해결 할 수 있는 문제는 아닌듯 하다. 간신히 해결(https://github.com/realgrid/intra.realgrid.com/issues/9)
* aws EC2에 새로운 instance를 만들고 ssh로 접속 할때 다음과 같은 메시지를 만난다면:

   <pre>
Warning: Identity file aws-wooritech.pem not accessible: No such file or directory.
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
Someone could be eavesdropping on you right now (man-in-the-middle attack)!
It is also possible that a host key has just been changed.
The fingerprint for the ECDSA key sent by the remote host is
SHA256:A5Gux2Z0rglng+5PnDjqFUJV8k6j142ZsooTrLVvMeo.
Please contact your system administrator.
Add correct host key in /Users/onlydel/.ssh/known_hosts to get rid of this message.
Offending ECDSA key in /Users/onlydel/.ssh/known_hosts:13
ECDSA host key for ec2-52-78-25-246.ap-northeast-2.compute.amazonaws.com has changed and you have requested strict checking.
Host key verification failed.</pre>

  설명에 나와있는 `known_hosts:13` 라인을 삭제 하고 다시 실행 하면 된다.

### Jul 27, 2016
* intra, www, support를 통합해서 하나의 db를 사용하기 위해 mupx deploy설정으로 같은 서버에 올라가 있는 컨테이너의 다른 인스턴스들 끼리 공유를 해보고자 MONGO_URL을 `mongodb://mondodb:27017/realgrid-support-dev`로 설정했지만 deploy할때 db에 연결 할 수 없다는 에러가 발생 한다. 반나절을 소모하고 원인을 docker container에 있다는 것은 알았는데([이슈](https://github.com/arunoda/meteor-up/issues/758)), 해결 하기위해 docker를 공부해야 하는 부담 때문에, 그리고 어차피 별도의 db서버를 가져가야 하는 것이 최종의 모습이기 때문에 mongolab에 계정을 만들고 500M짜리 무료 서비스를 설정했다. 나중에는 aws나 다른 클라우드 내에서 서비스를 구동하는 것으로 변경해야 한다.
* 외부 db사용할때 deploy는 mupx config에 적어 주면 되지만 로컬에서 테스트 할때는 연결정보를 환경변수에 담아 주어야 한다.

   <pre class="prettypring">
   $ export MONGO_URL='mongodb://user:password@paulo.mongohq.com:12345/'
   $ echo MONGO_URL
   $ unset MONGO_URL
   </pre>

### Jul 26, 2016
* mongoDB shell에서 collection을 조회 할때 잘 정리된 형태로 데이터를 보려면 ..find().pretty()하면 된다. 그런데 매번 pretty()를 호출 하려면 힘드니 아예 find()할때 마다 pretty()가 자동으로 실행 되면 좋겠다.

  <pre class="prettypring">
  echo DBQuery.prototype._prettyShell = true >> ~/.mongorc.js
  </pre>
* 25일 미티어가 [1.4 릴리즈](http://info.meteor.com/blog/announcing-meteor-1.4)를 발표했다. mongoDB, node.js 버전을 업데이트 했다고 한다.

### Jul 25, 2016
* [미티어 쿡북](https://github.com/clinical-meteor/software-development-kit) : 코드를 통해 meteor의 실전을 익힐 수 있는 교재

### Jul 21, 2016
* 서버에서 알람기능 구현을 위해
  - [later.js](https://github.com/bunkat/later)
  - [backend timer service](http://stackoverflow.com/questions/38493081/how-to-write-a-backend-service-that-runs-on-a-timer)
  - [미티어에서는](https://atmospherejs.com/vsivsi/job-collection)

### Jul 20, 2016
* Slack연동을 위한 API package : [khamoud:slack-api](https://github.com/krishamoud/meteor-slack-api)
* Meteor Tip: array로 되어 있는 property에 item을 push하거나 array의 item 객체를 수정하는 mongodb query 작성법

<pre class="prettyprint">
//push item to array property
Meteor.users.update({_id: userId}, {$push:{"emails": newEmail}});

//set item value of array property
Meteor.users.update({_id: userId}, {$set:{"emails.0.address": newEmailAddress}});
</pre>

### Jul 17, 2016
* GitHub이나 BitBucket같은 도구로 이슈관리 할때 틈날때 마다 task들을 작게 쪼개서 이슈에 등록해 두고 이슈를 처리해가는 방식으로 작업하는게 지속적인 유지보수에 많은 도움이 된다.

### Jul 15, 2016
* Hexo, 알수 없는 이상한 오류에 30분 헤매다가 `hexo clear`로 해결 본다. 결국, 원인도 모르고 뭘 고쳤는지도 모른다.
>>>>>>> cb433c112b2f9dac6e455c6cfbdb01a34cebe4c4

### Jul 1, 2016
* 포럼 형식의 질문 답변 게시판 프레임웍은 https://www.discourse.org/ 가 갑인가?

### Jun 30, 2016
* 어쩌다 보니 그리드 디자이너의 화면설계가 나와버렸다.

### Jun 28, 2016
* 스스로 성과를 평가(평가라기보다는 검증)할 수 있는 방법
  - 과연 어떤 방법이 좋을까?
  - 깃허브의 커밋갯수를 활용하는건 어떨까? 일한 만큼 커밋의 갯수가 늘어난다. 물론 갯수보다는 일의 가중이 중요하겠지만... 당장 손쉽게 할 수 있는 방법이 아닐까? 역시 이 방법은 좋은것 같지 않다..
  - 주 단위로 검증할 수 있는 방법이 뭐가 있을까? 주 단위로 깃헙을 체크한다? 깃헙을 체크 한다는 것은 참여도를 판단 하는 것이지 평가나 검증과는 거리가 좀 있다.
* Atom에 teminal을 embed하고 싶어 패키지를 검색하다 term3를 발견했다. 내가 원한 딱 그거다. 약간의 버그는 있지만 참고 쓸만하다. 헌데, 한글이 입력이 안된다. 이런... ㅠ.ㅠ git commit 할때 전부 영문을 쓰기엔 내 영어 실력이 거시기 하다.

### Jun 26, 2016
* [Meteor Night Jun 23](http://livestream.meteor.com)에서 [GraphQL](http://graphql.org/)과 [Apollo](http://www.apollostack.com/)를 만났다.
    - GraphQL은 페이스북에서 만든 데이타쿼리언어다. 이제 SQL은 가고 GQL이 오는 건가? 아직 먼 얘기일 수도 있겠지만 트렌드의 흐름이 어떻게 바뀌지 직접 사용해 보고 느껴볼 필요가 있겠다.
    - Apollo는 Meteor그룹에서 만든(아마도??) GraphQL 기반의 data stack이다. 미티어 자체가 client-side data stack을 가지고 있는 구조였는데 아마도 그 subscription 부분과 server-side 의 publication부분을 하나의 독립된 패키지로 분리하려는 시도가 아닌가 생각된다. 물론 오늘 하루 잠깐본 사이에 모든걸 다 알 수는 없지만, 앞으로 좀더 공부해 보고 실습해 보기로 한다.

### May 30, 2016
* 여러 Meteor 서비스를 한 서버에 배포하는 방법
    - Nginx vhost를 이용해 도메인 재분배: [https://github.com/arunoda/meteor-up/wiki/Using-Meteor-Up-with-NginX-vhosts#dynamic-vhost-is-it-possible](https://github.com/arunoda/meteor-up/wiki/Using-Meteor-Up-with-NginX-vhosts#dynamic-vhost-is-it-possible)
    - Nginx configuration: [https://www.linode.com/docs/websites/nginx/how-to-configure-nginx](https://www.linode.com/docs/websites/nginx/how-to-configure-nginx)
* Meteor Up 기존 배포 삭제 - [http://docs.meteor.com/commandline.html#meteordeploy](http://docs.meteor.com/commandline.html#meteordeploy), [http://stackoverflow.com/questions/10686320/how-do-i-undeploy-a-meteor-application](http://stackoverflow.com/questions/10686320/how-do-i-undeploy-a-meteor-application)

### Apr 1, 2016
* 안치환, 그 새벽같은 목소리의 노래를 들으면 기운이 난다.

### Mar 31, 2016
* 말수가 적어진다는 것은 할 말이 없는 것이 아니라 말 할 필요가 없거나 말 해도 소용이 없는 경우 일 수 있다.
* 기계식 키보드 소리 너무 거슬린다. 열심히 일하는 애들한테 머라 할 수도 없고... 에효~ :(

### Jan 25, 2016
* animation test day 1 [http://javascript.info/tutorial/animation](http://javascript.info/tutorial/animation)

### Jan 12, 2016
* [마이크로프트 Adapt - 음성인식 오픈소스](https://adapt.mycroft.ai)

### Jan 11, 2016
* [ReactJs를 이해하다.(번역글)-링크](http://blog.coderifleman.com/post/122232296024/reactjs를-이해하다1)
* [online book : Programming Javascript Applications - Eric Elliott](http://chimera.labs.oreilly.com/books/1234000000262/index.html)

### Dec 24, 2015
* javascript가 더이상 웹 전용이 아니라는 사실을 확인시켜주는 자료들.
    - [node-webkit(nw.js) samples](https://github.com/nwjs/nw.js/wiki/List-of-apps-and-companies-using-nw.js)
* 나를 미치게 만들었던 게임, 심시티. 그를 능가하는 게임([시티바운스](http://cityboundsim.com))을 만들고 있는 또 한 사람([Anselm Eickhoff](http://aeplay.co))
* AWS에서 몇 백원씩 과금 되던 놈, 원인을 찾았다. 예전에 node를 설치한 AMI 이미지를 저장해 놓고 있었는데 snapshot을 저장하는 elastics block storage는 free tier에 해당사항이 없기 때문이었던것 같다. 이런 detail한 과금 체계는 장점인가? 단점인가?


### Dec 22, 2015
* ES6에서 mixins 지원하지 않는 다고 한다. 더 쉬운 방법으로 비슷한 기능을 제공한다고 하니 그때까진 어쩔 수 없겠구먼.

### Dec 11, 2015
* React 책을 하나 구입했다. 번역된 eBook이다. 일주일 목표로 읽어본다. 알고있는 내용은 스킵하고 이틀동안 러프하게 한 번 읽으면서 간단한것만 실습하고 , 3일간 다시 한번 보면서 나머지 실습한다.
*

### Dec 1, 2015
* 나프다콘(10/31)이후 AWS에 계정을 만들고 이것저것 테스트를 진행 중이다. 물론 우리회사같은 구멍가게에서 클라우드는 언감생심(焉敢生心)이나 미래를 위한 준비라 생각하고 연구하고 있다. 게다가 1년간 제공되는 무료사용 서비스가 있고(물론 조금만 실수하면 과금이 되기도 하지만...) 2016년초에 한국내 리전(Region)을 개설한다는 소식때문에 약간 들떠 있는 분위기도 있다. 그렇지만, 회사내에 적용하려고 할때 동료들의 이유없는 반항에 대해 궂이 도입이유를 납득시켜야 하는 번거로움과 수고를 (또) 해야한다는 생각에 미리 지치기도 한다.

### Nov 23, 2015
* Javascript는 알면 알수록 어려운 언어인것 같다. 게다가 찾으면 찾을 수록 넘쳐나는 관련 기술들은 단숨에 확인하고 정리하기엔 너무도 광범위하다. 차근 차근 연구할 필요를 다시한번 느낀다.

### Nov 17, 2015
* ASP.NET 5에는 [common DI(Dependency Injection) 인터페이스](https://github.com/aspnet/DependencyInjection)가 만들어져 있고, 추가 라이브러리도 있는데,
    - [https://github.com/structuremap/도.dnx](https://github.com/structuremap/structuremap.dnx)
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

### May 20, 2015
* 슬랙과 깃헙을 전사적으로 활용하기 위해 아이디를 만들것을 동료들에게 제안했다. 이유없는 반발들이 돌아왔다. 회의적이다. 이 일이 정말 그렇게 귀찮은 일인가? 일을 위한 일을 만드는 것인가? 허탈하고 의지가 박탈된 기분이다. 슬랙과 깃헙에 혼자서 두개의 아이디를 만들어 이것 저것 연구했던 한달이란 시간이 이렇게 허무하게 느껴지다니... 나는 도대체 무엇 때문에 이런 짓을 하고 있는 것인가? 그냥 아무것도 안하고 회사의 프로세스가 어디로 흘러가건 상관없이 지켜보고 같이 표류하는게 옳은 일인가? 지친다.

### Apr 25
* 깃헙에 2013년 12월 18일 처음 아이디를 만들었었다. 사실 그 당시에 깃헙은 그냥 버전관리 저장소 정도로 생각했다. 더구나, 우리 회사는 이미 SVN을 사내서버에 구축해 사용하고 있었기 때문에 별다른 필요성을 느끼지 못했고, 깃헙에 대한 연구는 흐지부지 해졌다. 1년이 훌쩍 넘은 지금, 개인 블로그를 만들기 위해 여러가지 방법을 찾던 중 우연히 jekyll에 대해 알게 되었고, 깃헙을 기반으로 웹사이트를 구축 할 수 있다는 사실에 무작정 jekyll과 깃헙에 대한 공부를 시작하게 되었다. 이틀 만에 RealGrid의 document를 이곳에서 서비스하면 좋겠다는 생각을 하게 되었고 바로 준비작업에 들어갔다. 생각보다 쉬운 방법과 다양한 서비스의 연계를 경험하며 좀더 넓은 세계에 발을 들여놓은것 같다는 생각이 든다.
