---
title: "[Python Basic] 파이썬 기초 - 조건문(if문)"
header:
  #overlay_image: /assets/images/unsplash-image-1.jpg
  #caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  #actions:
    #- label: "Learn more"
      #url: "https://unsplash.com"
categories:
  - Python
tags:
  - python
  - programming
  - jupyter
  - jupyter notebook
  - data analysis
  - python basic
last_modified_at: 2022-11-29T12:51:00-00:00
---

#### condition(조건문)
 * 특정 조건을 만족하는 경우에만 수행할 작업이 있는 경우 사용
 * 모든 조건은 boolean으로 표현됨(예외 존재)
 * if, elif, else 키워드가 사용
 * 조건문의 경우, if, elif, else 블록에 종속된 코드는 들여쓰기로 표현 가능
 * 즉, 아래 코드에서와 같이 조건문 아래에 들여쓰기된 2줄의 코드만이 조건문의 조건에 따라 수행될 수도, 수행되지 않을 수도 있는 코드라고 할 수 있음
 * 들여쓰기 된 코드를 블록(block), 또는 코드블록이라고 함
 * python에서 모든 블록의 시작점의 마지막에는 :(콜론, colon) 추가 필요   
    
```python
if 6 >= 5:
    print('6 is greater than 5')
    print('Yeah, it is true')
print('This code is not belongs to if statements')
```
      
   
* Logical AND,OR,NOT
 * 조건문에 사용되는 조건의 경우, boolean이기 때문에 논리식 AND, OR, NOT 사용 가능
 * AND : and
 * OR : or
 * NOT : not
* 논리표
 * AND
  * True AND True : True
  * True AND False : False
  * False AND True : False
  * False AND False : False
 * OR
  * True OR True : True
  * True OR False : True
  * False OR True : True
  * False OR False : False
 * NOT
  * NOT True : False
  * NOT False : True
* 우선순위
  * NOT > AND > OR

   

**if의 조건이 bool이 아닌 경우**
   
* 일반적으로 조건문에는 bool이 주로 위치함
* 하지만 정수, 실수, 문자열 리스트 등 기본 타입도 조건에 사용 가능
* Flase로 간주되는 값(각 타입의 기본값)
 * None
 * 0
 * 0.0
 * ''
 * [] -> 빈 리스트
 * () -> 빈 튜플
 * {} -> 빈 딕셔너리
 * set() -> 빈 집합
* 그밖에는 모두 True로 간주
   
   
**if,else**
* if가 아닌 경우, 나머지 조건을 표현하고 싶다면 바로 아래 else 블락 사용
* 이 경우, if 조건이 True인 경우, if 블락의 코드가 수행. 거짓인 경우 else 블락의 코드가 수행
* 주의할 점: if와 else 사이에 다른 코드 삽입 불가
   

   
**if, elif, else**
* 조건이 여러개인 경우, 다음 조건을 elif블록에 명시 가능
* 이 경우, 각 조건을 확인 후 True인 조건의 코드 블록을 실행한 후, 전체 if, elif, else구문을 종료
* 조건문을 사용할 때는 if 이후, 0개 이상의 elif 사용 가능하며 0개 또는 1개의 else 사용 가능함
   

````python
a = 17
if a % 4 == 0:
    print('a is divisible by 4')
elif a % 4 == 1:
    print('a % 4 is 1')
elif a % 4 == 2:
    print('a % 4 is 2')
else:
    print('a % 4 is 3')
````
   
**중첩 조건문(nested condition)**
* 조건문의 경우 중첩하여 작성 가능
* 중첩의 의미는 depth(깊이)로 생각할 수 있으며, depth의 제한은 없음
   

