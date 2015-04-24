---
layout: post
title: About
permalink: /about/
---

This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](http://jekyllrb.com/)

You can find the source code for the Jekyll new theme at: [github.com/jglovier/jekyll-new](https://github.com/jglovier/jekyll-new)

You can find the source code for Jekyll at [github.com/jekyll/jekyll](https://github.com/jekyll/jekyll)

페이지를 여기서 바로 수정하면 반영되는가?
시간이 좀 걸려서 그렇지 반영은 바로 되는게 맞는것 같다.

# LocalDataProvider

> GridView를 위한 지역 메모리 Data provider이다. 그리드의 모든 행을 메모리에 순서대로 보관한다.    


{아노테이}

* 2차원 배열이라고 생각하면 된다.
* 행별로 key를 유지하지 않는다.
* 각 행은 실제 데이터를 가지고 있지 않을 수도 있다.
* hasData 함수로 실제 데이터가 있는 지 확인 할 수 있다.
* Sorting이나 Filtering은 이 원본 데이터 변경 없이 아이템 모델 수준에서 관리된다.
* 데이터셀(행 * field)의 변경이나, 행의 추가/수정/삭제 시 실행 전후 콜백 수준의 이벤트가 발생하고, 아이템모델을 거쳐 최종 클라이언트(그리드)에게 전달된다.
* 하나의 LocalDataProvider에 하나 이상의 클라이언트(그리드)가 연결될 수 있다. (Web 버전에서는 아직 제한되고 있다)

- wiki의 문서포멧은 표준 markdown과 비교해서 약간 차이가 있다.
+ 지속적인 작업을 위해 wiki문서를 markdown문서로 변환해 줄 필요가 있다.
+ 물론 툴을 사용해서 가능하겠지만...

[DataProvider](dataprovider.md)



<http://example.com/>

'''
    var options = {};
    options.style = "exclusive";
    grdMain.sortingOptions(options);
'''
