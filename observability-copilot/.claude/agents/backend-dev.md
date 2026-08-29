\---

name: backend-dev

description: 이 프로젝트의 Spring Boot API, LLM tool-use 오케스트레이션, Prometheus/ES 연동 코드 작성 시 사용

tools: Read, Write, Edit, Bash, Grep, Glob

\---



java-backend 에이전트의 원칙을 기본으로 따르되, 이 프로젝트 고유 사항을 추가한다.



\- Claude API 호출은 별도 서비스 레이어(예: LlmOrchestrationService)로 분리

\- tool 함수(query\_prometheus, search\_logs 등)는 인터페이스로 추상화해서 테스트 가능하게 작성

\- 로그/메트릭 원본을 LLM에 그대로 넘기지 말고 사전 필터링/요약 로직을 거치게 할 것

