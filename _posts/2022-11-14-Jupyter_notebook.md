---
title: "[Python Basic] 주피터 노트북 기본 사용법 02. 마크다운"
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
last_modified_at: 2022-11-15T23:38:00-00:00
---

### Jupyter Notebook 기본 사용법   
   
Jupyter Notebook 설치에 이어 본격적인 사용법을 익힙니다. 주피터 노트북은 파이썬 외에도 다양한 프로그래밍 언어를 사용할 수 있는데, 기본적으로 마크다운(Markdown) 역시 지원하고 있습니다.   
   
#### 마크다운(Markdown)이란?   
   
텍스트 기반의 마크업 언어. 2004년 존 그루버에 의해 만들어졌으며, 현재는 가장 대중적인 마크업 언어 중 하나. 버튼을 클릭하고 포맷 안에 글을 작성하면 즉각적으로 결과물을 볼 수 있는 WYSIWYG(What You See Is What You Get)와는 완전히 다릅니다. 마크다운 포맷의 파일을 생성할 때는, 마크다운 자체의 구문을 이용하여 실제로 보여지는 것과는 전혀 다른 방식으로 작성하게 됩니다.    
   
![image](https://user-images.githubusercontent.com/97453781/201944478-84d487bb-5194-48b2-8b73-93a644c3e6f0.png)   
   
마크다운 공식 페이지에서 전달하는 설명에 의하면, 마크다운 작성 원리는 위의 그림과 같이 총 4가지 절차를 이룹니다.
1. 텍스트 편집기 또는 전용 마크다운 애플리케이션을 이용하여 Markdown 파일을 만듭니다. Markdown파일의 확장자는 ".md" 또는 ".markdown" 입니다.
2. 마크다운 애플리케이션에서 Markdown 파일을 엽니다.
3. 응용 프로그램을 통해 html 문서로 변환합니다.
4. 웹 브라우저에서 html 파일을 보거나 Markdown 애플리케이션을 사용하여 pdf와 같은 다른 파일 형식으로 변환합니다.
      
##### 마크다운의 장점
1. 간결하다.
2. 별도의 도구없이 작성가능하다.
3. 다양한 형태로 변환이 가능하다.
4. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
5. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
6. 지원하는 프로그램과 플랫폼이 다양하다.

##### 마크다운의 단점
1. 표준이 없다.
2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
3. 모든 HTML 마크업을 대신하지 못한다.
      

#### 마크다운 사용법

##### header
      
```
This is an H1
=============
```   
   
This is an H1
=============   
      
```
This is an H2
-------------
```

This is an H2
-------------   
   
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
      
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6


##### block quote
   
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```
      
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.

```
> #### This is a header
> * List
> ```
code
> ```
```
   
> #### This is a header
> * List
> ```
code
> ```

   
##### list
   
```
1. first
2. second
3. third
```
   
   
1. first
2. second
3. third
   

```
1. first
3. third
2. second
```     

1. first
3. third
2. second
