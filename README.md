# portfolio
#### 기본에 충실하고자 하는 포트폴리오 <br>
---

## 📃 목차
- [오즈의제작소 클론 사이트](#오즈의제작소-클론-사이트)
- [폴인 클론 협업 프로젝트](#)
- [매거진 서비스 클론 사이트](#)
- [아모레퍼시픽 클론 사이트](#)
- [기타 경험: AI / Flutter / 오픈소스](#기타-경험)

***

## ✨ 오즈의제작소 클론 사이트 |  React + Open AI  <br>

### 🗨 소개
굿즈 커스터마이징 기업의 서비스를 클론하여 개발한 반응형 웹앱 쇼핑몰입니다. <br> 상품마다 옵션이 다양해 상세페이지에서 선택 시 자동으로 가격이 계산됩니다.

외부 데이터를 활용해 상품을 등록하며, OpenAI 기반 챗봇 기능으로 상담 편의성을 높였습니다. <br> 실제 서비스 구현을 위해 AWS 환경에 배포하였습니다.

### 🗓️ 기간
2025.06.09 ~ 2025.07.28 (약 1개월)

### 👥 인원
1명 (프론트엔드, 백엔드)

### 🛠️ 주요 기능 구현
- OpenAI API 연동 및 백엔드 대화 기능 구현
- Docker, MySQL 설정 및 리눅스(Ubuntu) 환경에서 데이터베이스 구축
- AWS 설정 및 도메인 연결, API 연동
- 백엔드 파일 POST/GET 요청 처리 및 데이터 작성 로직 구현
- 매거진 카테고리 영역에 CRUD 기능 적용
- 4 Depth Nav 탭바 구현 및 로직 설계
- Swiper를 활용한 반응형 웹앱 UI 개발 및 CSS 스타일링


### 🐛 이슈 리포트

> **4 Depth 탭 이슈** : **뎁스별 ID 중첩으로 탭이 열리지 않는 <br> 문제를 인덱스 세분화 및 로직 분할로 해결함.**
- 4 Depth 내비게이션 탭에서 데이터 구조 엉킴 문제 발생 복잡한 메뉴 구조를 구현하는 과정에서 <br> 뎁스별로 ID 값이 겹치면서 탭이 제대로 열리지 않는 문제가 반복적으로 발생했어요. <br>
  
  특히 3뎁스로 진입하는 구조가 꼬여 의도한 UI 동작이 이뤄지지 않았고, <br> 로직을 한 번에 짜기엔 난이도가 높아 각 단계별로 분리해 구성했어요. <br>

  인덱스를 세분화하고 ID 충돌을 피하는 방향으로 로직을 정리하면서 점차 문제를 해소했습니다. <br>


> **MySQL 데이터 누락 이슈: 로컬과 서버 간 데이터 불일치를 Docker 재빌드 및 API 재테스트로 수정함.**
- MySQL 데이터 누락 및 서버 반영 오류 로컬 테스트에서는 데이터가 정상적으로 출력되었지만, <br> 실제 운영 환경에선 일부 데이터가 누락되는 현상이 있었어요.
  
  <br> MySQL에는 데이터가 잘 들어가 있음에도 불구하고 UI에 나타나지 않거나 API 호출에 반응하지 않아, <br> 서버와 Docker 컨테이너 상태를 우분투 환경에서 직접 확인했어요.
  
  <br> 명령어 기반 디버깅과 MySQL 설정 재점검 후, Docker를 재빌드하고 <br> Postman으로 API 테스트를 반복한 끝에 데이터 삽입이 정상적으로 작동하도록 수정했습니다.


### ⚙️ 기술 스택
- **Framework**: Next.js, Express, React, TypeScript, Tailwind CSS, PostCSS
- **Database**: MySQL
- **CI/CD**: Vercel, GitHub Actions
- **Infra**: AWS EC2, AWS S3, RDS, Docker, Ubuntu, Node.js, nodemon
- **Testing & Mocking**: Postman, MSW, @mswjs/http-middleware
- **Monitoring & Debug**: TanStack React Query Devtools, ESLint, VSCode
- **AI Integration**: OpenAI API
- **UI/UX & Web Features**: Swiper

### 🔗 링크
- [✅ Distribution Site](https://www.hbjaws.com/)
- [‍💻 Frontend Repository](https://github.com/hbang012/oz-frontend)
- [💾 Backend Repository](https://github.com/hbang012/oz-backend)
- [💡 Chatbot Repository](https://github.com/hbang012/oz-chatbot)
  
---

## ✨ 폴인 클론 협업 프로젝트 | React

### 📍 소개
전문가의 경험을 공유하는 콘텐츠 기반의 웹 매거진 서비스입니다. <br> 세미나 페이지 중심으로 총 5개의 서브 화면을 직접 구현하였습니다.

기존 UI/UX를 분석해 화면 흐름을 설계하고 역할 분담을 조율했으며, <br> GitHub 레포지토리 관리 및 버전 컨트롤을 담당에 기여했습니다.

실 데이터를 활용하는 방법을 익히기 전, Mock 서버를 만들어 <br> 각자 페이지별로 가상의 데이터를 기반으로 작업을 진행했습니다.

### 🗓️ 기간
2025.04.04 ~ 2025.04.24 (15일)

### 👥 인원
3명 (프론트엔드)

### 🛠️ 주요 기능 구현
- 세미나 메인/상세 페이지 포함 총 5개 서브 UI 화면 구현
- 필터 상태 기반 조건부 렌더링 및 버튼 텍스트/스타일 동적 전환 로직 구현
- 세미나 데이터 흐름 설계 및 filterState, onClickHandler 중심 상태 제어 기능 구현
- 팀원 간 병렬 작업을 고려한 일정 조율 및 비동기 데이터 대응 로직 구축
- 로그인 페이지 UI 구현 및 비밀번호 보기/숨기기 상태 핸들링 기능 적용
- 다양한 해상도 테스트를 통해 반응형 디자인 최적화 및 시각적 정돈성 반영

### 🐛 이슈 리포트
> **협업 이슈 : ID 기반으로 mock 데이터 매칭해 협업 난이도 완화.**
- 기존 매거진 사이트의 데이터 로직이 복잡해 mock 데이터를 기반으로 <br> Mock 서버를 구성했으며, 팀원별 페이지 단위로 데이터를 나눠 작업했습니다.

  제가 담당한 영역에서 다른 팀원이 만든 데이터와 매칭하는 과정에서 구조 해석과 연결이 쉽지 않았고, <br> 이를 최소화하기 위해 ID 기반으로 항목을 구분하고 맞춰가는 방식으로 문제를 완화했습니다.


### ⚙️ 기술 스택
- **Framework**: React, React Router, Vite, TypeScript, Tailwind CSS, Styled-components
- **Database**: RESTful 구조 기반 외부 데이터 연동
- **CI/CD**:  Vercel, GitHub Actions
- **Infra**: Node.js, Vite, Ubuntu(Local), MSW
- **Testing & Mocking**: MSW, TanStack React Query Devtools
- **Monitoring & Debug**: ESLint, VSCode, React Query Devtools


### 🔗 링크
- [✅ Distribution Site](https://folin-cyp.vercel.app/)
- [🐙 GitHub Repository](https://github.com/hbang012/folin-cyp)

---

## ✨ 매거진 서비스 클론 사이트 | 

### 📍 소개
계좌 생성/해지 및 잔액을 기반으로 거래를 처리하는 REST API

### 🗓️ 기간
2025.05.07 ~ 2025.05.26 (2주)

### 👥 인원
1명

### 🛠️ 주요 업무
- Redis 기반 동시성 제어
- AOP를 활용한 재사용 가능한 분산락 구현

### ⚙️ 기술 스택
- Spring Boot, Spring Data JPA
- H2, Embedded Redis

---

## ✨ 공공 와이파이 검색 웹 서비스

### 📍 소개
사용자 위치를 중심으로 가까운 공공 와이파이 정보를 제공하는 웹 서비스

### 🗓️ 기간
2023.11.28 ~ 2023.12.17 (3주)

### 👥 인원
1명 

### 🛠️ 주요 업무
- 공공데이터 OpenAPI 활용
- 위치 기반 와이파이 검색 기능 구현

### ⚙️ 기술 스택
- **Framework**: React, React Router, Vite, TypeScript, Tailwind CSS, Styled-components
- **Database**: RESTful 구조 기반 외부 데이터 연동
- **CI/CD**:  Vercel, GitHub Actions
- **Infra**: Node.js, Vite, Ubuntu(Local), MSW
- **Testing & Mocking**: MSW, TanStack React Query Devtools
- **Monitoring & Debug**: ESLint, VSCode, React Query Devtools


### 🔗 링크
- [✅ Distribution Site](https://folin-cyp.vercel.app/)
- [🐙 GitHub Repository](https://github.com/hbang012/The-Singles)
---


---

## 📮 연락처

> ✉ 

