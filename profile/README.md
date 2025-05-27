# 🤖 WGA: Cloud Native MCP AIOps
> AWS 기반 클라우드 운영 자동화를 위한 서버리스 에이전트 플랫폼

![image](https://github.com/user-attachments/assets/66731b3c-754c-4cf2-9c31-cfd0371767c1)

---

## 🔍 Overview

WGA(WeGoAWS)는 클라우드 운영의 복잡성과 인력 부족 문제를 해결하기 위해 개발된  
**Cloud Native 기반의 지능형 AIOps Agent 시스템**입니다.

LLM(Large Language Model)과 MCP(Model Context Protocol)를 결합하여  
Slack 및 Web UI에서 실시간 로그 분석, 비용 최적화, 문서 검색, 다이어그램 시각화까지 지원하며  
**운영 자동화 및 의사결정 보조 시스템**으로 활용할 수 있습니다.

---

## 🤔 Why?

> “AWS의 복잡성을 줄이고, 운영 자동화를 위한 직관적인 인터페이스가 필요하다.”

### ✅ Cloud 환경의 문제점
<details><summary><b>1. Cloud 수요 증가와 통합 관리의 한계</b></summary>
- 클라우드 도입률 증가
- MSA 기반 파편화된 시스템 구조
- 통합 관리 어려움 & 전문 인력 부족
</details>

<details><summary><b>2. 복잡한 콘솔 & 로그 환경</b></summary>
- 다양한 서비스 콘솔 탐색과 학습 비용 부담
- CloudTrail, GuardDuty 등 로그의 분산
- Athena 쿼리 기반 분석의 진입 장벽
</details>

<details><summary><b>3. 실시간 대응과 문서 검색의 비효율</b></summary>
- CloudWatch 대시보드 분산
- 문서 검색 시 다국어 처리, 최신성 부족
</details>

---

## 🛠️ Features

### ✅ 주요 기능 개요
<details><summary><b>1. MCP 기반 자연어 질의</b></summary>

- Claude 3.7 Sonnet 등 다양한 모델 연동
- 문맥 기반 멀티턴 대화 및 세션 관리
- LLM ↔ MCP ↔ 로그 분석 도구 자동 연동

</details>

<details><summary><b>2. 실시간 로그 분석</b></summary>

- CloudTrail, GuardDuty, Lambda 등 통합 로그 접근
- 시간/사용자/IP 단위 분석, SQL 자동 생성
- 보안 이상 징후 탐지 및 시각화 지원

</details>

<details><summary><b>3. 비용 최적화 분석</b></summary>

- 일별/지역별/서비스별 비용 Breakdown
- 인스턴스 타입별 추천, 비용 급증 탐지
- 트렌드 기반 비용 시각화

</details>

<details><summary><b>4. AWS 공식 문서 검색</b></summary>

- 공식 문서 자동 검색 및 질문 기반 추천
- 한국어 번역 및 요약 제공 (기술 용어 보존)
- 페이지네이션 지원

</details>

<details><summary><b>5. 시각화 및 다이어그램 생성</b></summary>

- 차트 15종 지원 (Line, Bar, Pie, Network 등)
- AWS 아키텍처 다이어그램 자동 생성
- Python Diagrams 기반, 한글 폰트 설정

</details>

<details><summary><b>6. Slack 연동 챗봇</b></summary>

- `/models` 명령어로 모델 선택
- 대화 히스토리 기반 연속 질의
- 사용자 인증 기반 보안 통신

</details>

<details><summary><b>7. 보안 및 인증</b></summary>

- AWS Cognito, IAM 기반 인증/인가
- OAuth 2.0 및 OIDC 지원
- CORS 정책 기반 도메인 보호

</details>

<details><summary><b>8. 완전한 서버리스 아키텍처</b></summary>

- Lambda 기반 마이크로서비스 구성
- CloudFormation 기반 IaC 완전 자동화
- Amplify + CodeBuild + S3 + API Gateway 통합

</details>

---

## 🧩 Architecture

![architecture](https://github.com/user-attachments/assets/2dea6181-5280-46ec-a144-55a413020ffd)

- **LLM** ↔ **MCP** ↔ **운영 도구** 간 데이터 흐름
- Slack, Web에서 동일한 백엔드 공유
- 모든 응답은 실시간으로 MCP Tool 호출 → 결과 기반 LLM 응답 생성

---

## ⚙ CI/CD
![image](https://github.com/user-attachments/assets/2cabbaa7-b921-4330-9a5a-ccaa33ec56da)

---

## ✌️Member
| 이름 | 학과 | 이메일 | 역할 |
| --- | --- | --- | --- |
| 이민서 | 사이버보안학과 | mmmm@ajou.ac.kr | 팀장, Frontend |
| 황신철 | 사이버보안학과 | schwang2001@ajou.ac.kr | Backend, CI/CD |
| 김종민 | 사이버보안학과 | por8724@ajou.ac.kr | DB |
| 신명권 | 사이버보안학과 | dnu8894@ajou.ac.kr | Slackbot |
