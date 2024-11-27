# 📖 도서 판매 서비스 누리의 서재
- 개발 기간 : 2024.10.14 ~ 2024.12.06 (약 8주)
- 배포 URL : nuribooks.shop

<br>

## 프로젝트 소개

- 회원가입하면 5000원 무료 쿠폰 지급! 단언컨대 누리의 서재는 선택이 아닌 필수입니다.
- 도서 목록을 검색하여 특정 도서를 주문 및 조회 가능한 서비스입니다.  

<br>

## 팀원 구성

<div align="center">

| **김경민** | **김장현** | **박문순** | **이용택** | **이정규** | **임건우** | **정누리** | **정보호** |
| :------: |  :------: | :------: | :------: | :------: |  :------: | :------: | :------: |
| [<img src="https://avatars.githubusercontent.com/u/110990435?v=4" height=100 width=100> <br/> @kkyongg](https://github.com/kkyongg) | [<img src="https://avatars.githubusercontent.com/u/106305007?v=4" height=100 width=100> <br/> @Jkim052](https://github.com/Jkim052) | [<img src="https://avatars.githubusercontent.com/u/110738173?v=4" height=100 width=100> <br/> @hxcva1](https://github.com/hxcva1) | [<img src="https://avatars.githubusercontent.com/u/143694269?v=4" height=100 width=100> <br/> @itaekit](https://github.com/itaekit) | [<img src="https://avatars.githubusercontent.com/u/174286944?v=4" height=100 width=100> <br/> @ljg0610](https://github.com/ljg0610) | [<img src="https://avatars.githubusercontent.com/u/44187187?v=4" height=100 width=100> <br/> @rjsdn0124](https://github.com/rjsdn0124) | [<img src="https://avatars.githubusercontent.com/u/115128881?v=4" height=100 width=100> <br/> @yeon-so](https://github.com/yeon-so) | [<img src="https://avatars.githubusercontent.com/u/174286636?v=4" height=100 width=100> <br/> @Jprotection](https://github.com/Jprotection) | 

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

## 2. 브랜치 전략

- Git-flow 전략을 기반으로 main, develop 브랜치와 feature 보조 브랜치를 운용했습니다.
- main, develop, Feat 브랜치로 나누어 개발을 하였습니다.
    - **main** 브랜치는 배포 단계에서만 사용하는 브랜치입니다.
    - **develop** 브랜치는 개발 단계에서 git-flow의 master 역할을 하는 브랜치입니다.
    - **Feat** 브랜치는 기능 단위로 독립적인 개발 환경을 위하여 사용하고 merge 후 각 브랜치를 삭제해주었습니다.

<br>

## 4. 역할 분담
    
### 💕김경민

- 도서 기여자, 태그
- 쿠폰

### 💣김장현

- 도서 카테고리
- 쿠폰

### 🦒박문순

- 장바구니
- 환불

### 🐳이용택

- 인증
- 배송, 포장

### 🍕이정규

- 도서
- MQ 설정

### 💩임건우

- CI/CD
- 검색
- 포인트,리뷰

### 👻정누리

- 인증(부)
- 주문

### 🍀정보호

- 회원


<br>
