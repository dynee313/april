# Chapter 3 "시스템 설계 면접 공략법 / 효과적 면접을 위한 4단계 접근법"

## 단계별 요약

* 1단계. 문제 이해 및 설계 범위 확정
* 2단계. 개략적인 설계안 제시 및 동의 구하기
* 3단계. 컴포넌트 상세 설계
* 4단계. 마무리

## 1단계. 문제 이해 및 설계 범위 확정

* 의미 있는 질문을 통해 요구사항과 가정을 분명히 하여 모호함을 없애야 한다.
* 시스템 구축을 위해 필요한 정보를 모으자.

### 예제: 뉴스 피드 시스템 설계

* 모바일 앱/웹 지원? 둘다 지원
* 가장 중요한 기능은 무엇인지? posting, 친구들과 피드 기능을 볼 수 있어야 함.
* 정렬 기준? 시간 역순
* 친구를 맺을 수 있는 유저 수? 5000명
* 트래픽 규모? DAU(일간 능동 사용자. daily active user) 1000만명
* 포스트에서 지원하는 파일 양식? 이미지나 미디어같은 파일

## 2단계. 개략적인 설계안 제시 및 동의 구하기

* 설계안에 대한 최초 청사진을 제시하고 의견을 구하라.
* 화이트보드나 종이에 핵심 컴포넌트를 포함하는 다이어그램을 그려라. 
<br>(모바일/앱 클라이언트, API, 웹 서버, 데이터 저장소, 캐시, CDN, 메시지 큐 등)
* 필요한 경우, 이 최초 설계안이 시스템 규모에 관계단 제약사항들을 만족하는지를 개략적으로 계산하여 추정해 보라.

### 예제: 피드 발행 및 피드 생성

<img src="https://blog.kakaocdn.net/dn/kAvty/btsIUUu66ZC/ok6jSlEk2X2jq8RG3Zm250/img.png"
alt="https://thewayitwas.tistory.com/597">

## 3단계. 상세 설계

* 불필요한 세부사항에 시간을 쓰지 말고, 설계 대상 컴포턴트 사이의 우선순위를 정해야 한다.
* 가장 중요한 컴포넌트부터 설명하기 시작하라.
* 질문에 따른 답변 초점 예시
    * 시스템의 성능 특성에 대한 질문 - 시스템의 병목 구간이나 자원 요구량 추정치에 초점
    * 단축 URL 생성기 - 이 해시 함수의 설계를 구체적으로 설명
    * 채팅 시스템 - latency를 줄이고 사용자의 온/오프라인 상태를 표시할 것인지에 대한 답변

> 즉, 면접관의 의도를 파악하고 긍정적 시그널을 전달하는데 집중해야 한다.

### 예제: 피드 발행과 뉴스 피드 가져오기 기능에 대한 상세 설계

* 메시지 큐, 캐싱, DB, 서버에 대한 추가 정보를 상세화

<img src="https://blog.kakaocdn.net/dn/cDzZyo/btsITVIjUZ9/KRUH69iZ3nKwQOTKgaPPo1/img.png"
alt="https://thewayitwas.tistory.com/597">

## 4단계. 마무리

* 시스템 병목 구간 등 개선 가능한 지점을 인지하자. (비판적 사고 능력, 좋은 인상)
* 오류가 발생하면 무슨 일이 생기는지(서버 오류, 네트워크 장애 등)를 따져보자.
* 운영 이슈 관리 - 메트릭은 어떻게 수집하고, 모니터링은 어떻게 할 것인지.
* 미래에 닥칠 규모 확장 요구에 대한 대처

> 포기하지 말고, 소통을 주저하지 말라.

## 시간 배분

* 1단계 - 문제 이해 및 설계 범위 확정 (3m - 10m)
* 2단계 - 개략적 설계안 제시 및 동의구하기 (10m - 15m)
* 3단계 - 상세 설계 (10m - 25m)
* 4단계 - 마무리 (3m - 5m)

## Reference

* https://thewayitwas.tistory.com/597
