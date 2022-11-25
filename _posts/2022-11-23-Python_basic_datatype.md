---
title: "[Python Basic] 파이썬 기초 - 데이터 타입의 이해"
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
last_modified_at: 2022-11-23T23:28:00-00:00
---

### string(문자열)
- 복수개의 문자를 순서대로 나열한 것
- 문자열은 '(작은 따옴표) 혹은 "(큰 따옴표) 사이에 문자를 넣어서 생성
- 문자열 자체에 ',"가 있는 경우에는 각각 그 반대의 기호로 생성

**''' ''' 사용하여 표현 가능**
- 차이점
 - '', "" -> 따옴표(', ")를 양쪽으로 둘러싸기: 한줄 문자열 표현
 - ''' ''' -> 따옴표(',") 3개를 연속으로 써서 양쪽으로 둘러싸기: 여러줄에 걸쳐 문자열 표현 가능
   
```python
a = '"Hello" World'
b = "'Hello' World"
c = "Hello World. It's wonderful world"

print(a)
print(b)
print(c)
```
```
>>> "Hello" World
>>> 'Hello' World
>>> Hello World. It's wonderful world
```   

```python
multiline = "Life is too short. You need python."
print(multiline)
multiline = '''
Life is too short.
You need python.
'''
print(multiline)
multiline = """
Life is too short.
You need python.
"""
print(multiline)

```   
```
>>> Life is too short. You need python.
>>> Life is too short.
    You need python.
>>> Life is too short.
    You need python.
```   
   

**escape string (이스케이프 문자)**   
* 문자열내의 일부 문자의 의미를 달리하여 `특정한 효과`를 주는 것
* `\n` : new line `\t` : tab 등   

```python
print('Hello World \n\n')
print('Ha\thahahaha')
```
```
>>> Hello World


>>> Ha	hahahaha
```      

**indexing & slicing string (문자열 인덱스 및 추출)**
* 문자열의 각 문자는 순서가 있음
* 이때 각 문자열의 순서를 **인덱스**라고 함
* 첫번째 문자부터 마지막까지 차례대로의 순서를 가짐
* 첫번째 시작 문자의 순서는 0으로 시작(1이 아님)
   
   
* **연습문제** 문자열의 마지막 문자 순서의 값은?   
```python
a = 'Hello World' # 길이: 11
print(a[10])
```

**-1 인덱스**
* 다른 언어와는 달리, python의 경우 음수 인덱스를 지원
* -1이 가장 마지막 인덱스를, -2가 마지막에서 두번째 인덱스를 의미 ...

```python
print(a[0])
print(a[10])

print(a[-1])
print(a[-11])
```   

**인덱스의 범위**
* 인덱스는 [0, 문자열의 길이]의 범위만 유효
* 음수 인덱스를 사용할 경우, [-문자열의 길이, -1]
* 범위를 넘어갈 경우 에러 발생
      
```python
print(a[11])
print(a[-12])
```

**문자열 slicing**
* 인덱스가 하나의 문자만을 추출한다면,
* slicing은 부분 문자열을 추출한다고 볼 수 있음
* [시작:끝]과 같이 명시하여 [시작, 끝]에 해당하는 부분 문자열을 추출
* 시작, 끝 인덱스가 생략되어 있다면, 0부터 혹은 끝까지로 간주
   
   
```python
a = 'Hello world'
print(a[0:4])
print(a[1:7])

print(a[:5])
print(a[3:])
``` 
   
**문자열 함수** 
* 문자열은 여러가지 기능 제공을 위한 함수 내장
* 함수란 특정 기능을 하는 코드로, 언제든지 호출하여 해당 기능을 사용 가능하도록 구성한 코드
* 추후 함수에 대해 자세히 다룰 예정
```python
a = 'hello world'
a.upper()
```

* **replace**
 * 문자열 내의 특정 문자를 치환
    
```python
a = 'hello world'
a.replace('h','j')
```   

* **format**
 * 문자열 내의 특정한 값을 변수로부터 초기화하여 동적으로 문자열 생성 
    
```python
temperature = 25.5
prob = 80.0

a = "오늘 기온 {}도이고, 비 올 확률은 {}%입니다.".format(temperature, prob)
print(a)
```

   
* **split**
 * 문자열을 특정한 문자 구분하여 (delimiter) 문자열의 리스트로 치환
   
```python
a = "hello world what a nice weather"
a.split() # 기본은 띄어쓰기
```   
```python
a.split('w')
```


### 리스트 & 튜플
* 복수개의 값을 담을 수 있는 데이터 구조
* 실생활에서 사용하는 리스트(학생 리스트, 성적 리스트 등)과 동일한 의미로 이해
* list - mutable(생성된 후에 변경 가능)
* tuple - immutable(생성된 후에 변경 불가능)