---
title: "[Python Basic] 파이썬 기초 - @staticmethod"
header:
categories:
  - Python
tags:
  - python
  - programming
  - jupyter notebook
  - data analysis
  - python basic
last_modified_at: 2022-11-23T23:28:00-00:00
---

기본적으로 파이썬 클래스의 메서드는 인스턴스를 통해 호출해야 합니다.   
예를 들면,   
```python
class Counter:
    def __init__(self):
        self.num = 0
        
    def increment(self):
        self.num += 1
    
    def reset(self):
        self.num = 0
        

c1 = Counter() # 인스턴스 생성
c1.print_current_value() # 인스턴스를 통해 메서드 호출
c1.increment()
c1.reset()

```   
   
인스턴스를 통하지 않고도 클래스에서 바로 호출할 수 있는 메서드가 있습니다. 정적 메서드(static method)와 클래스 메서드(class method)입니다.      

먼저, 정적 메서드는 메서드 위에 @staticmethod 를 붙여서 작성합니다. 이때 매개변수에 self를 지정하지 않습니다.   
```python
class 클래스이름:
    @staticmethod
    def 메서드(매개변수1, 매개변수2):
        코드
```   

이렇게 생성한 메서드는 모듈의 함수를 사용하는 것과 유사한 방법으로 호출하여 사용할 수 있습니다.   
```python
class Math:
    @staticmethod
    def add(a, b):
        return a + b
    
    @staticmethod
    def multiply(a, b):
        return a * b
```
위와 같은 클래스와 정적 메서드가 있을 때,   
```python
Math.add(10, 20)
Math.multiply(10, 20)
```   
이런 방식으로 사용이 가능합니다. 
   
이러한 정적 메서드는 self를 받지 않기 때문에 인스턴스 속성에는 접근할 수 없습니다. 그래서 보통 정적 메서드는 인스턴스 속성이나 인스턴스 메서드가 필요하지 않을 때 사용합니다.    
   
정적 메서드는 메서드의 실행이 외부 상태에 영향을 끼치지 않는 순수 함수(pure function)를 만들 때 사용합니다. 부수 효과가 없고 입력값이 같으면 언제나 같은 출력값을 반환시킵니다. 즉, 정적 메서드는 인스턴스의 상태를 변화시키지 않는 메서드를 만들 때 사용합니다.   


참고 자료: [fastcampus](https://fastcampus.co.kr/), [코딩도장](https://dojang.io/mod/page/view.php?id=2379)