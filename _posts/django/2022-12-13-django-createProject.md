---
layout: post
title: Pokemon Project 만들기
date: 2022-12-13 21:30
description: django 프로젝트 만드는 과정
tags: django|python
---

프로젝트를 시작하기 위해 몇 번을 지웠는지 모릅니다.

이글을 보는 분들은 그런 일을 겪지 않기 위해서라도 순서를 기억하길 바랍니다.
> 사실 이 순서가 깔끔한 프로젝트를 만드는데 얼마나 큰 관여를 하는지 좀 더 공부할 필요가 있겠습니다.

<br>

## django 프로젝트 생성
> 1. github에 Repository 생성 및 local 폴더에 적용하기 - 이 부분의 자세한 내용은 github repository 생성 하다보면 중 자세한 설명을 볼 수 있으니 여기서는 축약했다.
> 2. Virtual Environment 만들기 (프로젝트 폴더 생성)
> 3. Virtual Environment 활성화하기
> 4. django 설치하기
> 5. django project 만들기
> 6. django app 만들기
> 7. 나만의 앱 만들기 시작하기

<br>

1~6번의 경우 django document의 초반에 너무 자세히 잘 나와있으니 참고하길 바랍니다.

다음 포스팅 부터는 7번을 하면서 새로 배운 내용이나 해결해본 issue를 다룰 예정입니다.

<br>

참고로 처음 적용할 기능은 아래와 같습니다.
1. API를 통해 포켓몬 리스트 가져와서 정보 띄우기
2. 특정 포켓몬 searching
3. 포켓몬 리스트 sorting