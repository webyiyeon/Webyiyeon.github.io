---
title: "[Python Basic] 주피터 노트북에서의 파이썬 기본 작성법"
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
last_modified_at: 2022-11-22T23:28:00-00:00
---
### = 대입 연산자, == 비교 연산자
- 대입의 경우, 오른쪽의 수식이나 값을 evaluation(여기서는 계산이라는 의미로 사용)한 뒤, 
- 왼쪽에 명시된 변수에 해당 값을 대입
- 변수는 해당 값을 가지게 됨   

```python
a = 10
b = 11.4
```   

### comment(주석)
- 코드에서 #으로 시작하는 뒷부분은 실행되지 않음
- python이 소스코드를 실행하면서 #을 만나면 무시
- 개발자(사람)가 보기 위한 용도로 사용    

```python
# this line is very important
# so don't delete those lines

a = 10
b = 11.4
```

### print 함수
- 함수란 특정 기능을 반복적으로 호출하여 사용가능한 코드블럭
- 해당 변수의 값을 출력
- ,로 여러 변수를 나열하면 한 줄에 출력
- 기본적으로는 한 칸 띄어쓰기 후 출력
   
```python
print(a, b)
print(a, 10, 200, b)
```   

### print 함수 설정
- sep : 구분자, 각 출력할 변수 사이에서 구별하는 역할을 함
- end : 마지막에 출력할 문자열

```python
print(a, b, 10, 100, sep='*', end='!!')
```   

### 변수 값 확인법
- print()함수 사용
- 변수 값을 코드의 마지막에 위치시킨 후 실행
 - 이 경우, output으로 변수의 값이 출력   

```python
print(a)
print(a, b)
a
```
   
### variable naming(변수 이름 규칙)
- 숫자로 시작하는 이름을 제외하고 영문 대소문자, _, 숫자로 구성 가능
- 아래의 예제는 모두 valid한 변수 이름
- 일반적으로 해당 변수를 표현하고자 하는 정확하고 간결한 이름을 사용하는 것이 원칙
 - 코드를 읽은 것을 더 쉽게 할 수 있음
 - e.g) a = 1000의 경우보다 **student_num = 1000** 로 명시한 것이 변수에 대한 이해가 빠름
    

```python
abcABC = 100
_abc124 = 200
ABC124 = 200
a456BC = 100

a = 200
number_of_students = 200
```   

