## 송호빈 (Hobin Song)

10년차 백엔드 개발자입니다. 상품 · 주문 · 결제 · 정산처럼 **틀리면 돈이 어긋나는 도메인**을 주로 다뤘습니다.

여행 플랫폼의 결제·구독·정산 시스템, 병원 CRM과 대용량 의료 데이터, 게임 서비스의 실시간 랭킹,
비대면 주문 서버와 POS 연동, 공공기관 상황관리 시스템까지 — 트래픽 성격과 정합성 요구가
서로 많이 다른 서비스들을 거쳤습니다.

### 기술

| 분야 | |
|---|---|
| 언어 | Java, Python |
| 프레임워크 | Spring Boot, Spring Data JPA, MyBatis, eGovFrame |
| 데이터 | MariaDB / MySQL, PostgreSQL, Redis, QueryDSL |
| 연동 · 비동기 | Stripe, RabbitMQ, 스케줄러 / 배치 |
| 인프라 | AWS (EC2, S3, LB), Docker, Linux, Nginx |

### 공개 프로젝트

**[storepay](https://github.com/hobinsong-dev/storepay)** — 클라우드 POS 결제 백엔드 API

가맹점이 여러 매장을 운영하고 각 매장의 POS 단말이 주문·결제하는 구조를 다룹니다.
동작하는 CRUD가 아니라, 결제 도메인에서 실제로 문제가 되는 지점을 설계로 어떻게 막았는지를
보여주는 데 목적이 있습니다.

- 총액을 클라이언트에게서 받지 않고 서버가 상품 마스터로 재계산 (단말 조작 차단)
- 주문 시점 단가 스냅샷 — 가격이 바뀌어도 과거 주문·영수증·정산은 불변
- 컬렉션 페이징과 fetch join 분리로 N+1 없이 정확한 페이징
- Flyway + `ddl-auto: validate` — 스키마 불일치는 기동 단계에서 실패
- Testcontainers로 실제 PostgreSQL에 마이그레이션까지 검증

`Java 17` `Spring Boot 3.5` `JPA` `QueryDSL` `PostgreSQL` `Flyway` `Docker` `GitHub Actions`

### 일하는 방식

코드를 많이 쓰는 것보다 **나중에 고치기 쉬운 상태로 두는 것**에 더 신경 씁니다.
그래서 "왜 이렇게 했는지"를 코드 주석과 README에 남기는 편입니다.

AI 코딩 도구(Claude Code)를 일상 개발에 쓰고 있습니다. 다만 생성된 코드를 그대로 쓰지는 않고,
프로젝트 규약과 도메인 설계 문서를 먼저 정의해 **아키텍처 일관성을 통제하는 방식**으로 운영합니다.
실무에서 이 체계를 팀 개발 표준으로 정리해 본 경험이 있습니다.

### 연락

- Email: shb514@naver.com
