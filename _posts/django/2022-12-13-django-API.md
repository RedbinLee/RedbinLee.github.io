---
layout: post
title: Pokemon API 불러오기
date: 2022-12-13 21:30
description: django에서 특정 외부 API 불러오기
tags: django python
---

만드려는 프로젝트에 꼭 필요한 요소가
포켓몬에 대한 List이다.

모든 포켓몬을 하나하나 database에 입력할 수 있겠지만,
public open API를 사용해서 그 수고를 좀 덜고 싶었다.

<br>

django에서는 views.py에서 작업하는 방법을 선택했다.
> (아마 큰 프로젝트에서 사용하는 방식은 다를거라 생각된다.)

<br>

처음에는 RESTful API를 사용해야 하나? 생각했는데 뭔가 훨씬 복잡해지는 것 같아 심플하게 requests library를 사용했다.
> (Restful API는 유저 로그인 기능 만들때 사용할 계획이다.)

<br>
library 설치 및 적용은 https://pypi.org/project/requests/에 잘 나와있으니 참고하시길 바라며,

<br>

### 특별히 유의해야 하는 부분은 data type 이었다.
> ### 각각 포켓몬 객체의 정보를 뽑을 때와 포켓몬 객체 리스트의 정보를 뽑을 때 json의 형태에 차이가 있었다.

<br>

내가 사용한 API는 json 파일로 내려받았으며 dictionary 형태를 띈다.
{% highlight python %}
response = requests.get('https://pokeapi.co/api/v2/pokemon/?limit=20&offset=20').json() # data_type : dictionary
{% endhighlight %}

<br>

이 dictionary 안에 List의 형태로 정보를 제공하고 있었다.
{% highlight python %}
response_info = response['results'] # data_type : list
{% endhighlight %}


<br>
오늘 과정에서는 API 읽는법, dictionary 처리 방법 등을 알아보는 시간이었다.