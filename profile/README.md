# 📖 갈등 판결 서비스 '몇대몇'

![Readme](https://github.com/user-attachments/assets/d0dc47aa-9c6c-4858-a102-6f4dadae7d83)

- 배포 URL : https://www.otoo.kr/
- Test ID : otoo
- Test PW : 1234

<br>

## 프로젝트 개요
아오, 답답해 누구한테 물어보지?! 누가 시원하게 대답해줘!<br/>
커뮤니티에 글을써서 물어보기는 과한거같고, 몰래 물어보고싶은데.. <br/>
우리 AI기반 웹서비스 몇대몇은 
여러 관계속에 오고가는 대화들을 명확하게 판결 해드립니다.<br/>
누가 맞았어! 대화속 시원한 판결
카카오톡, 챗봇 등 다양한 대화로 알아보는 판결

## 프로젝트 소개
- 음성, 텍스트, 이미지 모든 형태의 대화 데이터 기반으로 상황 판단 후 판결을 내려주는 서비스
- 서운함을 달래줄 언제나 내편, 무조건 맞장구 쳐주는 캐릭터 챗봇과 더불어 나의 감정을 추스려주는 감정리포트

## 리포지토리 목록

이 프로젝트는 다음과 같은 리포지토리로 구성되어 있습니다:

- [Frontend (React)](https://github.com/Team-A-I/otoo_react)
- [Backend (FastAPI)](https://github.com/Team-A-I/otoo_python_llm)
- [API Gateway (RestAPI)](https://github.com/Team-A-I/otoo_java)
<br>

## 팀원 구성

|<img src="https://avatars.githubusercontent.com/u/109562023?v=4" width="150" height="150"/>|<img src="https://avatars.githubusercontent.com/u/143330992?v=4" width="150" height="150"/>|<img src="https://avatars.githubusercontent.com/u/150677044?v=4" width="150" height="150"/>|<img src="https://avatars.githubusercontent.com/u/159854114?v=4" width="150" height="150"/>|
|:-:|:-:|:-:|:-:|
|권회은<br/>[@heweun](https://github.com/heweun)|김현석<br/>[@hyunseok92](https://github.com/hyunseok92)|정상엽<br/>[@catapracts](https://github.com/catapracts)|배정현<br/>[@baejeonghyun23](https://github.com/baejeonghyun23)|

<br>

## 1. 개발 환경

- Front :  React
- Back-end : RestAPI , FastAPI
- 버전 및 이슈관리 : Github, Github Issues, Github Project
- 협업 툴 : Slack, Notion, Github
- 서비스 배포 환경 : Netlify , AWS ECS
- 디자인/브래인스토밍 : Figma , Miro
<br>

## 2. 채택한 개발 기술과 브랜치 전략

### React

- React
    - 컴포넌트화를 통해 추후 유지보수와 재사용성을 고려했습니다.
    - 유저 배너, 상단과 하단 배너 등 중복되어 사용되는 부분이 많아 컴포넌트화를 통해 리소스 절약이 가능했습니다.
    
### FastAPI

- 속도와 성능
    - FastAPI는 Python의 최신 기능을 활용하여 높은 성능을 제공합니다. 특히 비동기 처리를 지원하여 요청을 빠르게 처리할 수 있습니다. 이는 LLM과 OCR 모델과 같은 고성능 연산이 필요한 작업에 적합하여 FastAPI를 사용했습니다.
- 확장성
    - FastAPI는 다양한 플러그인과 라이브러리를 쉽게 통합할 수 있어 확장성과 유지보수성이 뛰어납니다. 이를 통해 프로젝트의 요구사항 변화에 유연하게 대응할 수 있습니다.

### RestAPI

- JPA ORM (Java Persistence API)
    - JPA를 사용하면 객체 지향 프로그래밍 언어로 데이터베이스 작업을 수행할 수 있습니다. 이는 SQL을 직접 작성할 필요 없이 데이터베이스와 상호 작용할 수 있게 해줍니다.
    - 데이터베이스 테이블과 자바 객체 간의 매핑을 자동으로 처리해주는 JPA를 통해 데이터베이스 연동 코드 작성이 간소화되고, 유지보수성이 향상됩니다.
    - JPA는 데이터베이스 특정 기능에 대한 추상화를 제공하여, 다양한 데이터베이스를 쉽게 교체할 수 있는 유연성을 제공합니다.
    - 또한, JPA는 1차 캐시와 2차 캐시를 제공하여 데이터베이스 접근 성능을 최적화할 수 있습니다.
 
- Spring Security
    - Spring Security는 인증과 권한 부여, 공격 방어 (예: CSRF, XSS, 세션 고정)와 같은 다양한 보안 기능을 제공하여 애플리케이션의 보안성을 높일 수 있었습니다.
    - 다양한 인증 방식을 지원하며, 이를 쉽게 구성할 수 있습니다. 예를 들어, OAuth2, JWT, REDIS, REFRESH TOKEN 같은 기본 인증 등을 손쉽게 조합하여 사용할 수 있었습니다.
    - Spring Security는 Spring 생태계와 자연스럽게 통합되며, Spring Boot와 함께 사용하기 매우 용이합니다. 이는 보안 관련 코드를 쉽게 추가하고 관리할 수 있었습니다.

### 브랜치 전략

- Git-flow 전략을 기반으로 main, develop 브랜치와 feature , HotFix 보조 브랜치를 운용했습니다.
- main, develop, Feat 브랜치로 나누어 개발을 하였습니다.
    - **main** 브랜치는 배포 단계에서만 사용하는 브랜치입니다.
    - **develop** 브랜치는 개발 단계에서 git-flow의 main 역할을 하는 브랜치입니다.
    - **Feature** 브랜치는 기능 단위로 독립적인 개발 환경을 위하여 사용하고 merge 후 각 브랜치를 삭제해주었습니다.
    - **HotFix** 브랜치는 배포 단계에서 긴급하게 수정할 때 사용하는 브랜치입니다.

<br>

## 3. 프로젝트 아키텍처

![image](https://github.com/user-attachments/assets/571fc0b0-c442-456c-8f61-a62e979297c5)


<br>

## 4. 역할 분담

### 🍊권회은

- **UI**
    - 페이지 : 홈, 방명록, 업로드모달, 동의모달
    - 공통 컴포넌트 : 전역 글씨폰트, 버튼
- **기능**
    - Paddle OCR, 시스템 프롬프트 작성,  데이터 전처리, 방명록 등록 및 삭제, 중복코드 정리, 서브모듈 ,DB에 데이터 저장

<br>
    
### 👻김현석

- **UI**
    - 페이지 : 장구봇, 로그인/회원가입, 감정리포트, 관리자페이지(임베딩값 DB저장)
    - 공통 컴포넌트 : AXIOS설정
- **기능**
    - 장구 챗봇 , QnA챗봇, 감정리포트, Redis, Sercurity, ERD작성, RAG

<br>

### 😎정상엽

- **UI**
    - 페이지 : 관리자페이지, 마이페이지
- **기능**
    - 데이터 셋 만들기, 파이선 백 디버깅, 마이페이지, 관리자페이지 

<br>

### 🐬배정현

- **UI**
    - 페이지 : 업로드페이지, 음성업로드, 결과페이지
    - 공통 컴포넌트 : 버튼, Tip모달창
- **기능**
    - 배포, CI/CD 구축 , STT, Chat OpenAI, 리팩토링, 비동기처리, google Analytics4 
    
<br>

## 5. 개발 기간 및 작업 관리

### 개발 기간

- 전체 개발 기간 : 2024-12-19 ~ 2024-7-31
- 기획 및 회의 : 2024-06-19 ~ 2024-06-24
- 기획 발표 : 2024-06-25
- 환경설정 : 2024-06-26 ~ 2024-06-29
- 모델 테스트 및 사용 모델 확정 : 2024-07-01 ~ 2024-07-06
- 프로젝트 개발 : 2024-07-08 ~ 2024-07-20
- 배포 및 피드백 : 2024-07-21 ~ 2024-07-23
- 에러수정 및 피드백 수렴 : 2024-07-24 ~ 2024-07-26
- 문서 작업 및 발표 준비 : 2024-07-29 ~ 2024-07-30
- 최종발표 : 2024-07-31

<br>

### 작업 관리

- GitHub Projects와 Issues를 사용하여 진행 상황을 공유했습니다.
- 데일리 스크럼을 통해 매일 작업 상황을 공유하였습니다.
- 일주일에 한번씩 회고를 통해 부족한모습과 그대로 가져가야 할 점들을 정리하였습니다.

<br>

## 6. 신경 쓴 부분

- 빠른 개발 및 배포
    - 우리 팀은 초기 계획보다 절반의 시간 안에 프로젝트를 배포하는 데 성공했습니다. <br/> 이는 팀원들의 협력과 효율적인 개발 프로세스를 통해 가능했습니다.

- 피드백 수렴 및 개선
    - 1차 배포 후, 우리는 주변 지인들의 피드백을 적극적으로 수렴했습니다. <br/> 이를 통해 사용자 경험을 개선하고, 더 나은 기능을 구현할 수 있었습니다.

- 시장 반응 조사
    - 2차 배포에서는 커뮤니티 사이트에 프로젝트를 공개하여 시장의 반응을 살폈습니다. <br/> 이를 통해 다양한 사용자들의 의견을 반영하고, 프로젝트의 방향성을 더욱 명확히 할 수 있었습니다.

- 백로그 확인
    - 프로젝트를 실제 서비스처럼 구현하기 위해 Google Analytics 4(GA4)를 사용하여 데이터를 분석했습니다. 아래는 GA4 대시보드의 스크린샷입니다.
<p align="center">
  <img src="https://github.com/user-attachments/assets/ef537153-7ae5-4d48-9124-abe4756dec6e" alt="KakaoTalk_20240727_171605794_02" width="22%" />
  <img src="https://github.com/user-attachments/assets/8f54d469-2fd5-43e0-99e3-13829d62a683" alt="KakaoTalk_20240727_171605794_01" width="22%" />
  <img src="https://github.com/user-attachments/assets/d1ef55b1-8b1a-435b-b687-dd72bea5eaf9" alt="KakaoTalk_20240727_171605794" width="22%" />
  <img src="https://github.com/user-attachments/assets/05d63493-84a1-458b-9745-0579a087e19a" alt="KakaoTalk_20240727_171605794_07" width="22%" />
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/fc11df3e-8401-4f12-bedc-ac3704ffa4a8" alt="KakaoTalk_20240727_171605794_06" width="22%" />
  <img src="https://github.com/user-attachments/assets/c9dfec3e-8adc-4d6e-9c58-e554afa11ceb" alt="KakaoTalk_20240727_171605794_05" width="22%" />
  <img src="https://github.com/user-attachments/assets/1ff24683-8666-4cd7-95bd-b3626131ddef" alt="KakaoTalk_20240727_171605794_04" width="22%" />
  <img src="https://github.com/user-attachments/assets/e6f3a1dd-ad4c-4f26-b1fa-00b7e9741f15" alt="KakaoTalk_20240727_171605794_03" width="22%" />
</p>
<br>

## 7. 페이지별 기능

### [초기화면]

#### PC 버전

<p align="center">
  <img src="https://github.com/user-attachments/assets/ffd2585a-96c3-4864-a9df-3126f106df85" alt="메인화면(pc)" width="50%" />
</p>

#### 모바일 버전

<p align="center">
  <img src="https://github.com/user-attachments/assets/b1600369-d05f-44b6-8ee1-29dfba141eb1" alt="메인화면(mobile)1" width="25%" />
  <img src="https://github.com/user-attachments/assets/5073c578-232b-4373-b652-13294b3e6371" alt="메인화면(mobile)2" width="25%" />
</p>
<br>

### [회원가입]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/c084a491-c51e-4dfc-a588-9288d3504805" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
  <img src="https://github.com/user-attachments/assets/96da695a-5be6-4580-9176-772980af2718" alt="메인화면(mobile)2" width="25%" />
</p>
<br>

### [로그인]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/2c2c40cb-610c-4e61-9dd8-b898a7aa53f6" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
  <img src="https://github.com/user-attachments/assets/19cb2eda-ddf3-4dcf-9f31-b594db02dabe" alt="메인화면(mobile)2" width="25%" />
</p>
<br>

### [비밀번호 찾기]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/751d7b42-8326-4150-af16-1f9d949742c3" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
  <img src="https://github.com/user-attachments/assets/3438ac82-2561-42d6-985f-63095c30c2f4" alt="메인화면(mobile)2" width="25%" />
</p>

<br>

### [갈등판결(업로드 페이지)]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/b418eb6d-1152-4c43-9f47-de8d8be86eeb" alt="메인화면(mobile)1" width="40%" />
    <img src="https://github.com/user-attachments/assets/6f1886a0-7cad-4c2d-8513-8e9ae9dba98f" alt="메인화면(mobile)1" width="40%" />
    <img src="https://github.com/user-attachments/assets/73cfa9e5-7a13-404f-8171-d55160971c7c" alt="메인화면(mobile)1" width="40%" />
    <img src="https://github.com/user-attachments/assets/d8b15ba7-e1ba-4ccf-8c93-2b1b7b0b2e6b" alt="메인화면(mobile)1" width="40%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/ad29daa5-328e-416c-9585-2c5fe60bbe46" alt="메인화면(mobile)1" width="20%" />
    <img src="https://github.com/user-attachments/assets/9abbf96a-8009-41a7-8cba-3e57c3de0b50" alt="메인화면(mobile)1" width="20%" />
    <img src="https://github.com/user-attachments/assets/2f3cdddc-1531-4d2b-a05c-7bf0deca1223" alt="메인화면(mobile)1" width="20%" />
    <img src="https://github.com/user-attachments/assets/d55081af-1af5-45ba-9572-5a744556a50c" alt="메인화면(mobile)1" width="20%" />
</p>

<br>

### [로딩페이지]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/4eeceaee-f4f5-4f48-9db9-d1cd59332f5b" alt="메인화면(mobile)1" width="40%" />
    <img src="https://github.com/user-attachments/assets/b09f8411-b56a-485f-8703-2760355d3d79" alt="메인화면(mobile)1" width="40%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/69c1fb1d-9fdc-4c98-ac90-c06d23aa6f1b" alt="메인화면(mobile)1" width="25%" />
    <img src="https://github.com/user-attachments/assets/9292d2ce-63ff-400f-8a9e-77afe2af61f5" alt="메인화면(mobile)1" width="25%" />
</p>

<br>

### [갈등판결 결과페이지]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/0096bf7e-dc11-41b8-ae07-116872e67945" alt="메인화면(mobile)1" width="40%" />
    <img src="https://github.com/user-attachments/assets/fcacba87-9251-4276-964e-5deb322af95c" alt="메인화면(mobile)1" width="40%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/b263bdca-7bd1-47b4-9a92-cd377c0e39e1" alt="메인화면(mobile)1" width="25%" />
    <img src="https://github.com/user-attachments/assets/f2e5d37a-3ced-4c8d-81e4-87414dde6fce" alt="메인화면(mobile)1" width="25%" />
</p>

<br>

### [맞장구봇]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/062ae817-add8-40db-bf31-2d773461dc8d" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/fc00478f-44e3-497d-b562-ef814cd00407" alt="메인화면(mobile)1" width="25%" />
</p>

<br>

### [맞장구봇(일반모드)]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/6c5dbbee-487d-45d9-82ca-a740e88c1773" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/15fd9fbc-97ed-4e5f-bd2f-898dcf930cde" alt="메인화면(mobile)1" width="25%" />
</p>
<br>

### [맞장구봇(장구모드)]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/5c0e5f0d-81fc-41bd-a9ff-1b18fb62e22b" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/79a4355e-10ac-49ef-83f1-74d7b39600ca" alt="메인화면(mobile)1" width="25%" />
</p>

<br>

### [맞장구봇(감정리포트)]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/8e4d294e-bb66-45bf-a53b-e022359a3cbc" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/070aa8cd-2b11-4f6b-8782-c4a4136607c8" alt="메인화면(mobile)1" width="25%" />
</p>

<br>

### [Tip & Feedback]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/db6c0d7e-ab7d-4ac0-be2f-a0b1f9a218b2" alt="메인화면(mobile)1" width="40%" />
    <img src="https://github.com/user-attachments/assets/a3b835b5-a55b-4c9f-8ae3-e2b28c580157" alt="메인화면(mobile)1" width="40%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/392be124-97a1-4705-b195-274d8fab4771" alt="메인화면(mobile)1" width="25%" />
    <img src="https://github.com/user-attachments/assets/1772a62c-5a0e-46a2-8611-373fa705e870" alt="메인화면(mobile)1" width="25%" />
</p>

<br>

### [방명록]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/eae72e7d-aa0f-41d8-80fd-103ba4f071c0" alt="메인화면(mobile)1" width="40%" />
    <img src="https://github.com/user-attachments/assets/b84f3d08-5c17-4dad-94f0-787eacef8d2c" alt="메인화면(mobile)1" width="40%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/3ca69eb9-fedb-4066-b455-2d7f677d0c75" alt="메인화면(mobile)1" width="25%" />
    <img src="https://github.com/user-attachments/assets/ae2bdb55-a321-4221-b92e-9d0741562b9e" alt="메인화면(mobile)1" width="25%" />
</p>
<br>

### [QnA]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/995c6dcb-3cf3-4a9a-b51c-d05f6281c47e" alt="메인화면(mobile)1" width="50%" />
</p>

#### 모바일 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/7a07e0ef-ab77-45af-b070-bf3471973044" alt="메인화면(mobile)1" width="25%" />
</p>
<br>

### [관리자페이지]

#### PC 버전

<p align="center">
    <img src="https://github.com/user-attachments/assets/8a2a6396-d26e-440a-a2b2-e6b8a04b14e8" alt="메인화면(mobile)1" width="80%" />
</p>


<br>

## 8. 개선 목표

- 막상 배포를하고 시장에 내놓아보니 이용하는 사용자가 없는 일이 발생<br/>
  -> 사용자들이 우리 서비스를 사용해야 하는 이유를 찾아보고 개선 할 예정

- STT 음성 업로드는 현재 마이크 입력을통해 음성파일로 변환해 결과값을 받아오고있음 <br/>
  -> Websocket,gRPC 를 통해 실시간 스트리밍으로 전환해 사용자에게 말하고있는 내용을 시각적으로 보여 줄 예정
    
<br>

## 9. 프로젝트 후기

### 🍊 권회은

- 

<br>

### 👻 김현석

- 


<br>

### 😎 정상엽

- 6/3부터 7/31까지 진행한 프로젝트 내내 많은 것들을 배울 수 있었습니다. 다른 팀원분들이 약 99% 정도를 구현했고 제가 기여한 것은 1%정도라고 말해도 과언이 아닐 정도였습니다. 저와는 압도적으로 실력차이가 나는 다른 팀원들을 보며 많이 부족함을 느꼈고, 스스로 반성하는 시간이 되었고, 좀 더 자신을 갈고 닦아야 겠다는 마음이 들었습니다. 팀원들께 짐이 되어 죄송한 마음뿐입니다. 꼭 다들 성공하셨으면 좋겠습니다. 2달 동안 감사했습니다. 앞으로 좋은 일들만 가득하시길 바라겠습니다.
<br>

### 🐬 배정현

- 여러모로 많은 것들을 배울 수 있었던 한 달이었습니다. 각자 다른환경에서 학습을 하다 온 사람들과 만나서
  같이 프로젝트를 하다보니 내가 알고있는것이 전부가 아니였구나 다른방식, 더 나은방식이 있었고 그로인해 새로운 지식들을 접해볼 수 있는 좋은 기회였다고 생각이들었습니다.
  좋은 팀원들 덕분에 좋은길로 나아갈 수 있는 발판이 생겨 첫걸음을 내딛을 수 있었습니다. 모두들 수고하셨습니다. 감사합니다.
  
