---
title: "[Python] 파이썬 라이브러리 altair 데이터 시각화"
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
  - altair
  - chart library
last_modified_at: 2022-11-14T21:46:00-00:00
---
   
### Altair Chart Library 설치 및 기본 사용법   
   
altair library [link](https://altair-viz.github.io/index.html)   
   
#### Installation 설치
   
```
$ pip install altair vega_datasets
```
사용법을 연습하기 위해 vega dataset과 altair를 함께 설치하는 방법.   
   
```
$ conda install -c conda-forge altair vega_datasets
```
아나콘다 패키지를 사용한다면 vega dataset과 altair를 함께 설치하는 방법.   
      
      
## Overview

### Altair   
   
[Vega](http://vega.github.io/vega)및 [Vega-Lite](http://vega.github.io/vega-lite)를 기반으로 하는 Python용 선언전 통계 시각화 라이브러리.   
   
### How to use   
   
   
✅ **기본 사용법**
   
```python
import altair as alt

alt.Chart(판다스 데이터).mark_bar().encode(
	x = 'x축으로 지정할 컬럼명',
	y = 'y축으로 지정할 컬럼명',
	color = '색 분류할 컬럼명',
	tooltip = ['x축 컬럼명', 'y축 컬럼명', 'color 컬럼명'],
).properties(width=800, height=400).interactive()
```
   
- **`.mark_bar()`** : 차트 유형
- **`.encode(
	x = 'x축으로 지정할 컬럼명',
	y = 'y축으로 지정할 컬럼명',
	color = '색 분류할 컬럼명',
)`** : x축, y축, color, tooltip 등을 설정
- **`.properties(width=가로, height=세로)`** : width, height 등 속성 설정
- **`.interactive()`** : 추가 시 동적 차트로 변경(zoom 기능 등)

   
   
✅ 여러 그래프를 한 차트에 표현하고 싶을 때   
   
<img width="646" alt="altair example 01" src="https://user-images.githubusercontent.com/97453781/201663453-aabc2ce5-1e8c-4e1e-a48c-4aa221b75a34.png">
   
```python
import altair as alt
from vega_datasets import data

source = data.wheat() #표 형식의 데이터 
#		   year | wheat | wages 
# 0 |  1565 | 41.0  | 5.00 

bar = alt.Chart(**source**).mark_bar().encode(
    x='year:O',
    y='wheat:Q'
)

line = alt.Chart(**source**).mark_line(color='red').transform_window(
    # The field to average
    rolling_mean='mean(wheat)',
    # The number of values before and after the current value to include.
    frame=[-9, 0]
).encode(
    x='year:O',
    y='rolling_mean:Q'
)

(bar + line**).properties(width=600)
```
   
변수에 차트를 저장해서 더하기 연산(`+`) 또는 콤마(`,`)를 이용하여 한 차트에 표현 가능   
   
