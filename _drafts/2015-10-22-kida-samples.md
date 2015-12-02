---
layout: post
title: kida 샘플 화면 작성
date:   2015-10-21 13:24:23 +9:00 GMT
categories: 
  - Another Code
tags: 
  - html
  - jquery
  - parseHTML
  - iframe
---

https://docs.oracle.com/javase/tutorial/jdbc/basics/processingsqlstatements.html#executing_queries

jdbc로 db query 하는 코드는 대략 아래와 같다.

<pre class="prettypring">
if (v_sb.equals("b") || v_sb.equals("c")) v_tblgb = "busa_";

    if (v_gun.equals("z")) v_tblnm = v_libnm+v_tblgb+"y_sum";
    else v_tblnm = v_libnm+v_tblgb+"y_all";

  v_where = " p_rank = '"+v_rank+"' and           ";
  v_where+= " imkwan_gubun2 = '"+v_imkwan+"' and  ";
  v_where+= " skill2 = '"+v_skill+"' and          ";
  v_where+= " sex = '"+v_sex+"' and               ";
  v_where+= " gun = '"+v_gun+"'                   ";

    String st_query = null;
    st_query = " select * from "+v_tblnm;
    st_query += " where '@' = '@' and ";
  st_query += v_where;

    //out.println(st_query);
    rs1 = stmt.executeQuery(st_query);
</pre>

맨 마지막에 나오는 stmt.executeQuery()의 결과로 resultSet이 나오는데 이 ResultSet을 json으로 만들수 있으면 쉽게 데이터를 넣을 수 있게 된다.

별도의 jsp로 data를 제공해서 view를 분리 하는 방식으로 처리



---
**참조**

* [https://wolfpaulus.com/journal/mac/tomcat8/](https://wolfpaulus.com/journal/mac/tomcat8/){:target="_blank"}

