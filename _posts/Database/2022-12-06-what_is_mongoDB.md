---
title: "[MongoDB] 몽고디비란? - NoSQL DB"
header:
categories:
  - MongoDB
tags:
  - mongoDB
last_modified_at: 2022-12-01T23:44:00-00:00
---
#### SQL vs NoSQL 
**SQL**
- MySQL, PostgreSQL, SQLite
   

**NoSQL**
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

# MongoDB
      
대표적인 노에스큐엘(NoSQL) 데이터베이스 시스템. 몽고디비(MongoDB)는 데이터 교환 시 비산(BSON: Binary JSON) 문서 형태로 저장하여 여러 서버에 분산 저장 및 확장이 용이하며, 방대한 데이터 처리가 빠르다는 장점이 있다. MongoDB는 C++ 언어로 작성되었으며, 윈도우(Windows), 리눅스(Linux), 맥OS 등 다양한 운영 체제(OS)를 지원한다. 아페로 공용 라이선스(AGPL: Affero General Public License)에 따라 배포되는 공개 소스 소프트웨어(open source software)이다.   
[네이버 지식백과] 몽고디비 [MongoDB](https://terms.naver.com/entry.naver?docId=3435635&cid=42346&categoryId=42346) (IT용어사전, 한국정보통신기술협회)      
   

## MongoDB 소개 요약 
- 10gen사에서 개발한 솔루션(C++)
- Key-Value와는 달리 여러 용도로 사용 가능(범용적)
- 스키마를 고정하지 않는 형태
 + 스키마 변경으로 오는 문제가 없음
 + 데이터를 구조화해서 json형태로 저장(데이터를 key-value화 저장)
- join이 불가능하기 때문에 join이 필요없도록 데이터 설계 필요

## MongoDB 특징
- 메모리맵 형태의 파일엔진 DB이기 때문에 메모리에 의존적
 + 메모리 크기가 성능을 좌우
 + 메모리를 넘어서는 경우 성능이 급격히 저하됨
- 쌓아놓고 삭제가 없는 경우가 적합
 + "로그 데이터"
 + "이벤트 참여 내역"
 + "세션"
- 트랜잭션이 필요한 금융, 결제, 빌링, 회원정보 등에는 부적합 → RDBMS 사용

## Document data model
- 속성의 이름과 값으로 이루어진 쌍의 집합
- 속성은 문자열이나 숫자, 날짜 가능
- 배열 또는 다른 도큐먼트를 지정하는 것도 가능
- 하나의 document에 필요한 정보를 모두 담아야 함
- one query로 모두 해결이 되게끔 collection model 설계를 해야함
- join이 불가능하므로 미리 embedding시켜야함

**document data model: 데이터 설계를 "종이문서" 설계하듯이 설계해야한다.**

## JSON
- JSON: JavaScript Object Notation
 + lightweight data 교환 형식
 + 사람이 읽고 쓰기 쉽고, 기계가 파싱하고 생성하기 쉬움
 + JavaScript의 Array문법으로 데이터 구조를 기술하는 방법 → XML이 가진 유연성과 구조적 데이터 표현기능을 확보하면서, XML이 가진 오버헤드를 줄이는 방법으로 사용됨
 + 클라이언트에서 처리 퍼포먼스가 높음
 + XML이 표현하는 구조적인 정보 모두 표현 가능
 + 송수신 데이터로 XML을 사용하는 것에 비해 훨씬 빠르고 간편

- JSON 표기법
 + 각 객체는 중괄호({})로 시작하고 끝남
 + 문자열과 값으로 구성되어 있고, 콜론(:)으로 구분
 + 각 멤버들은 콤마(,)로 구분
 + 값은 object, string, number, array, true, false, null 사용 가능
 + 문자: 따옴표 사용, 숫자: 따옴표 사용 X
 + 배열: 대괄호([])로 시작하고 끝나며, 각 값은 콤마(,)로 구분

## MongoDB 장점
- Schema-less 구조:
 + 다양한 형태의 데이터 저장 가능
 + 데이터 모델의 유연한 변화 가능(데이터 모델 변경, 필드 확장 용이)
- Read/Write 뛰어남
- Scale Out 구조:
 + 많은 데이터 저장 가능
 + 장비 확장이 간단함
- JSON 구조: 데이터 직관적 이해 가능
- 사용 방법 쉽고, 개발이 편리함

## MongoDB 단점
- 데이터 업데이트 중 장애 발생 시, 데이터 손실 가능
- 많은 인덱스 사용 시, 충분한 메모리 확보 필요
- 데이터 공간 소모가 RDBMS에 비해 많음(비효율적인 Key 중복 입력)
- 복잡한 JOIN 사용시 성능 제약이 따름
- transactions 지원이 RDBMS 대비 미약함
- 제공되는 MapReuce 작업이 Hadoop에 비해 성능이 떨어짐
