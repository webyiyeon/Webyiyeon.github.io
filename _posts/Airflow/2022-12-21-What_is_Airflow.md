---
title: "[Airflow] 에어플로우(Airflow)란?"
header:
categories:
  - Airflow
tags:
  - Airflow
last_modified_at: 2022-12-21T20:45:00-00:00
---

# What is Airflow?

Apache Airflow [공식 사이트](https://airflow.apache.org/)

Apache Airflow는 workflow의 관리를 위한 오픈 소스 플랫폼입니다. Airflow Python 프레임워크를 사용하면 거의 모든 기술과 연결되는 워크플로를 구축할 수 있습니다. 웹 인터페이스는 워크플로 상태를 관리하는 데 도움이 됩니다. Airflow는 단일 프로세스에서 대규모 워크플로를 지원하는 분산 설정에 이르기까지 다양한 방식으로 배포할 수 있습니다.   

# 데이터 적재 파이프라인 생성
## DAG & Operator
+ DAG(Directed Acyclic Graph): 에어플로우의 핵심 개념이자 여러 작업들을 하나로 모으고 적절한 동작 수행을 위한 종속과 관계를 구성하는 역할을 합니다. 즉, 실행하고자 하는 작업들을 순서에 맞게 구성한 워크플로우(workflow)를 의미합니다. 


참조 링크:
[DAGs](https://airflow.apache.org/docs/apache-airflow/stable/concepts/dags.html)
[[Airflow] 데이터 적재 파이프라인 튜토리얼 - 서울시 지하철호선별 역별 승하차 인원 정보 적재하기](https://gibles-deepmind.tistory.com/133?category=954919)
[AirFlow DAG 소개와 기본 구조](https://www.bearpooh.com/151)

