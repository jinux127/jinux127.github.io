---
title:  "자바스크립트 기초 문법"
excerpt: "JavaScript"

categories:
  - JavaScript
tags:
  - JavaScript
last_modified_at: 2021-04-10T14:00-15:00

---

  

# 변수 var, let,const

JavaScript는 변수를 선언할 때, 자료형을 입력하지 않는다. var, let const 세가지 방식이 있다.

> # var
>
> - variable의 줄임말. 
> - var의 선언은 함수가 시작될 때 처리된다. 선언 위치가 어디든 상관없이 함수의 시작과 동시에 처리되기 때문에 선언보다 윗줄에서 변수가 참조되더라도 사용가능하다. 
> - 단, 선언만 하고 할당은 하지않는다.

> # let
>
> - var과 다르게 block 단위로 변수가 선언된다. 즉, 변수가 선언된 block에서만 사용 가능하다. 또한, 할당된 값 역시 바꿔줄 수 있다.

> # const
>
> - const로 변수 선언을 하면 let과 같이 block 단위로 변수가 선언되지만, let과 다른 점은 const는 변화하지 않는 변수. 상수이다.