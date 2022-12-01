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
last_modified_at: 2022-11-30T12:53:00-00:00
---
   
**loop(반복문)**
* 반복적인 작업을 가능하게 해주는 도구
* 특정 조건을 만족하는 경우 수행할 수 있음(while)
* 리스트, 문자열, 튜플 등 컬렉션 타입의 아이템을 하나씩 순회하면서 사용 가능(for)
* 코드 작업에서 가장 많이 사용하는 구문 중 하나
* 주의할 점: while을 사용할 경우, 반복을 멈추게 하는 장치가 필요
 * 그렇지 않으면 셀이 무한히 수행되며, jupyter notebook의 재부팅이 필요

      
**while 키워드**
* while 뒤의 조건이 True인 경우, while 코드 블록을 계속 수행
* while 코드 블록
 * if와 마찬가지로 while문 아래의 들여쓰기로 작성된 부분을 의미
* 조건이 False가 되면 블록 수행을 멈추고 이후 코드를 실행
      

**while 키워드를 이용하여 리스트 아이템 출력하기**
```python
a = [1, 10, 9, 24, 566, 23, 45, 67, 89]

i = 0 # 인덱스
while i < len(a):
    print('value: ', a[i], ', index: ', i)
    i += 1
    
print('hahah')
```

      
**while 키워드 이용하여 리스트 아이템 출력하기**
* 조건문과 함께 사용하기
```python
a = [1, 10, 9, 24, 25, 26]
i = 0 
while i < len(a):
    if a[i]%2==1:
        print(a[i])
    else:
        print(a[i]/2)
    i+=1
```
      
      
