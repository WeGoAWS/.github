## 🤖 AWS Cloud Agent: MCP-Based Cloud Native Agent for B2B IaC
![main](https://github.com/user-attachments/assets/d3fb10f6-57e9-4744-8dd5-f498baf96292)

</br>

## Why?

</br>

저희 WGA(WeGoAWS) 팀은 클라우드를 관리할 때, 어떤 기능이 있으면 좋을지 생각했습니다. 실제 현업자분들께 자문을 구한 결과, **챗봇을 통해 자연어 질의만으로 클라우드 운영 정보에 쉽게 접근할 수 있으면 좋겠다고 판단했습니다**. 서비스를 개발할 때, 다음과 같은 부분에 초점을 두었습니다.

</br>

<details> 
<summary><b>1. 복잡한 AWS 콘솔 탐색의 어려움</b></summary>
</br>

- 수많은 서비스와 메뉴 속에서 원하는 정보를 찾기 위해 여러 화면을 오가는 비효율성
- 각 서비스별로 다른 인터페이스로 인한 학습 비용 증가

</br>
</details>

<details> 
<summary><b>2. 로그 분석의 복잡성</b></summary>
</br>
  
- CloudTrail, GuardDuty 등 여러 서비스에 분산된 로그 데이터
- SQL 쿼리 작성 없이는 접근하기 어려운 Athena 기반 분석
  
</br>
</details>

<details> 
<summary><b>3. 실시간 모니터링과 대응의 어려움</b></summary>
</br>
  
- 분산된 CloudWatch 대시보드와 알람 확인의 복잡성
- 비용 분석과 최적화를 위한 데이터 수집의 번거로움
  
</br>
</details>

<details> 
<summary><b>4. 문서 검색과 학습의 비효율성</b></summary>
</br>
  
- 방대한 AWS 공식 문서에서 필요한 정보를 찾기 어려움
- 한국어로 번역된 최신 정보의 부족
  
</br>
</details>

</br>

서비스를 개발할 때, **자연어 질의를 통한 직관적 접근**, **실시간 데이터 분석**, **시각화를 통한 이해도 향상**에 초점을 두었습니다.

</br>

## Features
</br>

저희 서비스는 다음과 같은 핵심 기능을 제공합니다.

</br>

<details>
<summary><b>1. MCP 기반 지능형 자연어 질의 시스템</b></summary>
</br>

- **다중 AI 모델 지원**
  - Anthropic Claude 3.7 Sonnet (기본)
  - 사용자별 모델 선택 가능

- **고급 대화 처리**
  - 멀티턴 대화를 통한 문맥 이해
  - 세션 기반 대화 히스토리 관리
  - 복잡한 클라우드 운영 질문 해석

</br>
</details>

<details>
<summary><b>2. 실시간 로그 분석 및 인사이트</b></summary>
</br>

- **통합 로그 분석**
  - CloudTrail, GuardDuty, Lambda 등 다양한 서비스 로그
  - 자동 쿼리 생성 (에러 분석, 성능 분석, 보안 분석)
  - 시간대별/사용자별/IP별 상세 분석

- **인텔리전트 패턴 탐지**
  - 에러 패턴 자동 분류 및 빈도 분석
  - 의심스러운 로그인 패턴 탐지
  - 성능 메트릭 추세 분석

</br>
</details>

<details>
<summary><b>3. 비용 최적화 분석</b></summary>
</br>

- **다차원 비용 분석**
  - 일별/지역별/서비스별 상세 비용 분석
  - 인스턴스 타입별 비용 최적화 제안
  - 비용 급증 알림 및 트렌드 분석

- **시각적 비용 리포트**
  - 테이블 형태의 상세 비용 내역
  - 차트를 통한 비용 트렌드 시각화

</br>
</details>

<details>
<summary><b>4. AWS 공식 문서 검색 및 추천</b></summary>
</br>

- **지능형 문서 검색**
  - AWS 공식 문서 API 연동
  - 질문 맥락에 맞는 관련 문서 자동 추천
  - 페이지네이션을 통한 대용량 문서 처리

- **다국어 지원**
  - 한국어 자동 번역 및 요약 제공
  - 기술 용어 보존 및 정확한 번역

</br>
</details>

<details>
<summary><b>5. 동적 시각화 및 다이어그램 생성</b></summary>
</br>

- **15종류 차트 지원**
  - Line, Bar, Pie, Scatter, Area, Column 차트
  - Word Cloud, Radar, Histogram, Treemap
  - Dual-axes, Mind Map, Network Graph, Flow Diagram, Fishbone

- **AWS 아키텍처 다이어그램**
  - Python Diagrams 패키지 기반 자동 생성
  - AWS, K8s, On-premise 아키텍처 지원
  - 한글 폰트 자동 설정으로 완벽한 한국어 지원

</br>
</details>

<details>
<summary><b>6. Slack 통합 챗봇</b></summary>
</br>

- **슬래시 명령어 지원**
  - `/models` 명령어로 AI 모델 선택
  - DM을 통한 대화 인터페이스 제공

- **고급 인터랙션**
  - Block Kit을 활용한 인터랙티브 UI
  - 버튼 클릭, 드롭다운 선택 지원
  - 대화 히스토리 기반 연속 질의

</br>
</details>

<details>
<summary><b>7. 엔터프라이즈급 보안</b></summary>
</br>

- **다층 보안 인증**
  - AWS Cognito 기반 사용자 인증
  - OAuth 2.0 / OpenID Connect 표준 준수
  - Slack과 AWS 계정 연동 인증

- **세밀한 권한 관리**
  - IAM 역할 기반 API 접근 제어
  - 리소스별 세분화된 권한 설정
  - CORS 정책을 통한 도메인 보안

</br>
</details>

<details>
<summary><b>8. Cloud Native 서버리스 아키텍처</b></summary>
</br>

- **서버리스 컴퓨팅**
  - AWS Lambda를 통한 마이크로서비스 아키텍처
  - API Gateway 기반 RESTful API 설계
  - Auto Scaling과 고가용성 보장

- **Infrastructure as Code**
  - CloudFormation을 통한 완전 자동화
  - 환경별(dev/test/prod) 스택 분리
  - 원클릭 배포 및 롤백 지원

- **데이터 저장소**
  - DynamoDB를 통한 NoSQL 데이터 관리
  - S3 기반 정적 웹 호스팅
  - Athena를 통한 데이터 레이크 분석

</br>
</details>

</br>

## Member
| 이름 | 학과 | 이메일 | 역할 |
| --- | --- | --- | --- |
| 이민서 | 사이버보안학과 | mmmm@ajou.ac.kr | 팀장, Frontend |
| 황신철 | 사이버보안학과 | schwang2001@ajou.ac.kr | Backend, CI/CD |
| 김종민 | 사이버보안학과 | por8724@ajou.ac.kr | DB |
| 신명권 | 사이버보안학과 | dnu8894@ajou.ac.kr | Slackbot |
