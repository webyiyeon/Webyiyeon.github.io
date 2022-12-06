---
title: "[MongoDB] 몽고디비란? - NoSQL DB"
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
last_modified_at: 2022-12-01T23:44:00-00:00
---
#### SQL vs NoSQL 
*SQL*
- MySQL, PostgreSQL, SQLite

*NoSQL*
- Document, Graph, Key-Value 등 다양한 종류 존재 
- Document: MongoDB 
 * json document 형태로 저장 
 * 원하는 형태로 저장 가능 
 * 데이터의 형태가 같지 않아도 괜찮음
- Key-Value DB: CassandraDB, DynamoDB
 * CassandraDB
   + column wide database 유형이기도 함
   + 읽고 쓰기가 빠름
   + 애플, 넷플릭스, 인스타그램, 우버 등 
   + 검색엔진처럼 빠른 호출이 필요
 * DynamoDB
   + 아마존이 제작
   + 듀오링고(언어학습 앱): 매초 24,000개의 읽기 지원
   + 빠르게 많이 써야하고, 많이 읽어야할 때
   + 저장하기 전에 미리 어떻게 해야할지 구상해야함 
- GraphDB: column이나 document는 필요없지만, 노드 사이 관계를 알아야할 때
 * Tao
   + 소셜 네트워크에서 사용
   + 페이스북에서 제작 
   + 각각의 entity를 저장하고 이를 관계망으로 연결
 * neo4j


[노마드 코더] SQL vs NoSQL 5분컷 설명 [Youtube](https://youtu.be/Q_9cFgzZr8Q)

#### MongoDB
      
대표적인 노에스큐엘(NoSQL) 데이터베이스 시스템. 몽고디비(MongoDB)는 데이터 교환 시 비산(BSON: Binary JSON) 문서 형태로 저장하여 여러 서버에 분산 저장 및 확장이 용이하며, 방대한 데이터 처리가 빠르다는 장점이 있다. MongoDB는 C++ 언어로 작성되었으며, 윈도우(Windows), 리눅스(Linux), 맥OS 등 다양한 운영 체제(OS)를 지원한다. 아페로 공용 라이선스(AGPL: Affero General Public License)에 따라 배포되는 공개 소스 소프트웨어(open source software)이다.   
[네이버 지식백과] 몽고디비 [MongoDB](https://terms.naver.com/entry.naver?docId=3435635&cid=42346&categoryId=42346) (IT용어사전, 한국정보통신기술협회)      
   
