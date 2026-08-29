\# 관측성 코파일럿 프로젝트



\## 개요

Grafana/Prometheus 메트릭·로그를 자연어로 질의하고, 장애 시 LLM이 근본원인 후보를 요약하는 도구.



\## 스택

\- Backend: Java 17 / Spring Boot / Spring Batch + Quartz

\- 메시징: Kafka

\- 검색: Elasticsearch

\- 모니터링: Prometheus + Grafana

\- LLM: Claude API (tool use 기반, 프레임워크 없이 직접 구현)



\## 원칙

\- LLM 답변은 반드시 "가설" + 확신도 표기, 근거 원본 데이터 병기 (환각 방지)

\- 자동 조치(auto-remediation)는 절대 구현하지 않음 — MVP 스코프 아님

\- Phase 1: Prometheus 자연어 질의부터 시작, 순서대로 진행

