---
title: "[MongoDB] 몽고디비 쿼리문 작성법"
header:
  #overlay_image: /assets/images/unsplash-image-1.jpg
  #caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  #actions:
    #- label: "Learn more"
      #url: "https://unsplash.com"
categories:
  - MongoDB
tags:
  - mongoDB
  - programming
  - data
  - noSQL
  - data analysis
  - SQL
  - document data 
last_modified_at: 2022-12-12T23:44:00-00:00
---



### ✓ RDB와 MongoDB 용어 비교Permalink
   
RDB와 MongoDB 용어를 비교하는 경우 아래와 같습니다.

| RDB | MongoDB |
| --- | --- |
| Table | Collection |
| Row | Document |
| Column | Field |
| Primary Key | Object_Id Field |
|Relationship | Embedded & Link | 
   
   
### ✓ 비교(Comparison) 연산자
| operator | 설명 |
| --- | --- |
| $eq | (equals) 주어진 값과 일치하는 값 |
| $gt | (greater than) 주어진 값보다 큰 값 |
| $gte | (greater than or equal) 주어진 값보다 크거나 같은 값 |
| $lt | (less than) 주어진 값보다 작은 값 |
| $lte | (less than or equal) 주어진 값보다 작거나 같은 값 |
| $ne | (not equal) 주어진 값과 일치하지 않는 값 |
| $in | 주어진 배열 안에 속하는 값 |
| $nin | 주어진 배열 안에 속하지 않는 값 | 