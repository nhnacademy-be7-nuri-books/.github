# 📖 도서 판매 서비스 누리의 서재
- 개발 기간 : 2024.10.14 ~ 2024.12.06 (약 8주)
- 배포 URL : ~[nuribooks.shop](https://nuribooks.shop)~ (서비스 종료)

<br>

## 프로젝트 소개

- 회원가입하면 5000원 무료 쿠폰 지급! 단언컨대 누리의 서재는 선택이 아닌 필수입니다.
- 도서 목록을 검색하여 특정 도서를 주문 및 조회 가능한 서비스입니다.  

<br>

## 팀원 구성

<div align="center">

| **김경민** | **김장현** | **박문순** | **이용택** | **이정규** | **임건우** | **정누리** | **정보호** |
| :------: |  :------: | :------: | :------: | :------: |  :------: | :------: | :------: |
| [<img src="https://avatars.githubusercontent.com/u/110990435?v=4" height=100 width=100> <br/> @kkyongg](https://github.com/kkyongg) | [<img src="https://avatars.githubusercontent.com/u/106305007?v=4" height=100 width=100> <br/> @Jkim052](https://github.com/Jkim052) | [<img src="https://avatars.githubusercontent.com/u/110738173?v=4" height=100 width=100> <br/> @hxcva1](https://github.com/hxcva1) | [<img src="https://avatars.githubusercontent.com/u/143694269?v=4" height=100 width=100> <br/> @yongtaek2](https://github.com/yongtaek2) | [<img src="https://avatars.githubusercontent.com/u/174286944?v=4" height=100 width=100> <br/> @ljg0610](https://github.com/ljg0610) | [<img src="https://avatars.githubusercontent.com/u/44187187?v=4" height=100 width=100> <br/> @rjsdn0124](https://github.com/rjsdn0124) | [<img src="https://avatars.githubusercontent.com/u/115128881?v=4" height=100 width=100> <br/> @yeon-so](https://github.com/yeon-so) | [<img src="https://avatars.githubusercontent.com/u/174286636?v=4" height=100 width=100> <br/> @Jprotection](https://github.com/Jprotection) | 

</div>

<br>

## 1. 개발 환경

### 개발 환경
- 개발도구: Intellij IDEA - Ultimate
- 언어: Java 21 LTS<br>
- 빌드도구: Maven
- 개발
  - Spring Framework: 5.3
  - Spring Boot: 3.3.18
  - Spring Cloud
    - Spring Cloud Gateway
    - Spring Cloud Netflex(Eureka)
    - Spring Cloud Config
  - Spring Data
    - Spring Data JPA
    - Spring Data Elasticsearch
    - Spring Data Redis
  - JPA
    - QueryDSL
- 테스트
  - Junit5
  - AssertJ
  - Mockito
  - SonarQube
- 데이터베이스
  - MySQL: 8.0.25
  - Redis
- 검색엔진
  - Elastic Search: 7.11.1
- ERD
  - ERDCloud
- UI
  - BOOTSTRAP5
  - TOAST UI
- NHN Cloud
  - Instance
  - Secure Key Manager
  - Image Manager
  - Load Balancer
- 버전 및 이슈관리 : Github, Github Issues, Github Project
- 협업 툴 : Github Discussion
- [코드 컨벤션](https://github.com/orgs/nhnacademy-be7-nuri-books/discussions/13)
  
<br>

## 시스템 아키텍처
<img width="1035" alt="image" src="https://github.com/user-attachments/assets/89ceb3c0-4bca-4a04-9794-f2efa2c6efcd" />

## CI/CD
![image](https://github.com/user-attachments/assets/0a8e1392-da55-4503-8468-41fd9adf3d17)

## ERD
<p>https://www.erdcloud.com/d/ex62rEgj4hx77g4CA</p>

<br>

## 프로젝트 규칙

### 1. 브랜치 전략

- Git-flow 전략을 기반으로 main, develop 브랜치와 feature 보조 브랜치를 운용했습니다.
- main, develop, Feat 브랜치로 나누어 개발을 하였습니다.
    - **main** 브랜치는 배포 단계에서만 사용하는 브랜치입니다.
    - **develop** 브랜치는 개발 단계에서 git-flow의 master 역할을 하는 브랜치입니다.
    - **Feat** 브랜치는 기능 단위로 독립적인 개발 환경을 위하여 사용하고 merge 후 각 브랜치를 삭제해주었습니다.
 
### 2. 매일 9시 Scrum 진행

- Scrum 사항 및 공유 자료는 Discussion으로 공유하였습니다.
- [Discussions](https://github.com/orgs/nhnacademy-be7-nuri-books/discussions)

<br>

## 4. 역할 분담
    
### 🐰김경민

- 관리자 쿠폰 관리
	- 쿠폰 정책 등록, 조회, 수정, 만료 기능 구현
	- 쿠폰 발급 기능 구현(%쿠폰, 금액쿠폰, 도서쿠폰, 카테고리 쿠폰)
	- 회원가입시 웰컴 쿠폰 발급
	- spring batch를 활용한 생일 쿠폰 발급

- 도서(출판사, 기여자, 태그, 도서기여자, 도서태그)
	 - 등록, 조회, 수정, 삭제 구현

### 🐌김장현

- 도서 카테고리
  - 카테고리 등록, 삭제, 수정, 읽기 구현
  - 계층구조를 통해 5단계 뎁스 구현

- 쿠폰
  - 쿠폰 발급 로직 구현
  - 쿠폰 정책 등록 업데이트 구현
  - 배치를 통한 쿠폰 발급 구현

### 🦒박문순

- 장바구니
  - 회원/ 비회원 장바구니
  - Redis를 활용한 Caching
  - Redis Pub/Sub을 이용해 로그인 시 회원 장바구니 로드
  
- 회원
  - 회원 주소 기능
  - 도로명 주소 API 사용
    
- 환불
  - 환불 기능
  - 반품 요청 기능

### 🐳이용택

- 인증
  - 로그인, 로그아웃
  - 회원 상태에 따른 인증 처리
  - OAuth 2.0 적용 (Payco, Naver)
  - JWT 발급 및 재발급 처리
  - Access Token, Refresh Token 유효성 검증

- 주문/결제
  - 배송비 정책, 배송 관리
  - 포장지 관리
  - 비회원 주문 조회

### 🦄이정규

- 도서
  - 도서 직접등록, 외부 API 이용 등록기능 구현
  - 도서목록 조회, 상세 조회, 수정, 삭제 기능 구현
  - 좋아요 기능 구현
    
- 설정
  - 키매니저 설정
  - 이미지 매니저 설정
  - 로그백 설정
  - dbcp2 설정
    
- Message Queue
  - 재고 업데이트 RabbitMQ 적용
  - 도서쿠폰 발급 RabbitMQ 적용

### 🦝임건우

- CI/CD
    - GitHub Action을 이용한 CI/CD 구현.
    - NHN Cloud에서 동작하는 Spring 서버 자동 배포 Shell script 구현
    - 서버 이중화와 Eureka, Nginx를 활용한 무중단 배포 구현
- 리뷰
    - 회원의 주문 내역에 따른 리뷰 작성 및 수정 기능 구현
    - 이미지 업로드 및 별점 기능 추가
- 포인트
    - 포인트 규정 CRUD 구현
    - enum을 이용한 포인트 규정 별 전략 선택
    - 유저의 Event에 따라 EventListener 기반 포인트 적립 기능 구현
      
- Elasticsearch
    - Elasticsearch에서 nori 한글 분석기를 이용한 한글 검색 기능 구현
    - 데이터베이스와 동기화하기 위한 Logstash Docker를 이용하여 설정
    - 다양한 조건을 적용한 검색 필터링 기능 구현

### 👻정누리

- 인증
  - Eureka 기본 설정
  - Gateway 라우트, 필터 설정 
  - Jwt 토큰 재갱신 처리
    
- 주문/결제
  - 주문 등록, 조회(상세조회)
    - 주문 등록 : 회원/비회원 별개 등록 처리, 주문 내 포장, 쿠폰, 포인트 적용
  - 토스 페이먼츠 연동 결제 및 취소 처리

### 🦅정보호

- 회원
  - 회원 등록, 조회, 수정, 삭제 기능 구현
  - 다양한 검색 조건을 동적 쿼리로 작성하여 회원 검색
  - 회원 등급 등록, 조회, 수정, 삭제 기능 구현
    
- 배치
  - 마지막 로그인 일시를 기준으로 휴면 회원 전환
  = 탈퇴 일시를 기준으로 회원 정보 soft delete
  - 순수 결제 금액을 기준으로 회원 등급 업데이트

<br>
