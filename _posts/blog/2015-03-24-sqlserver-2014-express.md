---
layout: post
title: Microsoft SQLServer 2014 Express
date:   2015-03-12 21:13:31 +9:00 GMT
categories: 
  - EF
tags: 
  - EF
  - SqlServer
  - SqlServer 2014
---

### 들어가며
MS SQLServer 2014 Express에 대해 포스트 합니다.

* 에디션의 특징 및 라이선스
* 다른 에디션들과 차이점
* 다운로드
* 설치
* SQLManagement Studio에서 관리
* Visual Studio 2013 Community에서 관리

### 에디션의 특징 및 라이선스

https://msdn.microsoft.com/en-US/evalcenter/dn434043.aspx

https://msdn.microsoft.com/ko-kr/evalcenter/dn434042.aspx

https://msdn.microsoft.com/library/bb545450.aspx

### 다른 에디션들과의 차이점

Express 에디션은 다른 상용 에디션들과는 달리 무료로 사용할 수 있는 에디션이라는 점이 가장 큰 차이점이라고 할 수 있습니다. 물로 이외에도 성능이나 기능상의 많은 제약들이 있습니다. SQLServer 2014 각 에디션별 특징에 대해서는 [링크](https://msdn.microsoft.com/library/cc645993.aspx) 를 참조하시기 바랍니다.

https://msdn.microsoft.com/library/cc645993.aspx

Express Edition에는 몇 가지 버전이 추가되어 있습니다. 그 종류는

LocalDB(SqlLocalDB)
Express(SQLEXPR)
Express with Tools (SQLEXPRWT)
SQL Server Management Studio Express (SQLManagementStudio)
Express with Advanced Services (SQLEXPRADV)

### 다운로드

[에디션 소개 페이지](https://www.microsoft.com/en-us/server-cloud/products/sql-server-editions/sql-server-express.aspx)에서 다운로드링크를 찾아 클릭하면 다운로드 페이지로 이동합니다. 다운로드 페이지에서는 위에 소개된 몇 가지 버전을 선택한 다음 사용언어와 국가를 선택하고 다운로드 하면 됩니다.

### 설치

Express에디션을 설치하려면 설치 가능한 하드웨어 및 소프트웨어 요구사항을 확인해야 합니다. 하지만, Express에디션의 경우 성능이나 기능에 제약이 있는 만큼 많이 경량화되어 있기 때문에 이 에디션이 필요로 하는 시스템 요구사항은 다른 상용 에디션과 비교하여 훨씬 저렴한 요구사항임에는 틀림이 없습니다. 

메모리의 경우 다른 에디션들은 최소 1Gb, 권장 4Gb인데 비하여 Express에디션의 경우 최소 512Mb, 최대 1Gb입니다. 프로세스는 에디션과 관계없이 최소 1GHz(x86) ~ 1.4GHz(x64), 권장 2GHz이상이 필요합니다.

설치가능한 운영체제는 x86과 x64지원 버전에 따라 약간의 차이는 있지만 보통 Windows 7 이상의 운영 체제에서 모두 설치가 가능할 것으로 보입니다. 설치에 필요한 디스크 공간으로는 엔진 및 주요 기능을 설치하는데 811Mb정도의 공간이 필요합니다. 부가기능의 설치여부에 따라 별도의 공간이 필요할 수 있습니다.

보다 상세한 SQLServer 2014의 상용 에디션 및  Express에디션에 대한 하드웨어 및 소프트웨어의 요구사항에 대해 [링크](https://msdn.microsoft.com/ko-KR/library/ms143506%28v%3Dsql.120%29.aspx)를 참조하세요.

![](/images/blog/20150324-sqlserver-express-에디션선택.jpg)

### SQLServer ManagementStudio에서 관리


### VisualStudio Community 2013에서 관리


---
**참조**

* [https://msdn.microsoft.com/en-us/library/hh510202.aspx](https://msdn.microsoft.com/en-us/library/hh510202.aspx){:target="_blank"}