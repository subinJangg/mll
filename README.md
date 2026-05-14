# MLL MARKET (망링레 마켓)

망고, 링고, 레고 — 세 고양이의 이름을 딴 반려동물 쇼핑몰 웹 애플리케이션.

---

## 기술 스택

### Frontend
- Vue 3, Vue Router 4, Vuex 4
- Axios, Bootstrap 5, Font Awesome
- Daum 주소 검색 API

### Backend
- Spring Boot 2.2.4 (Java 8)
- MyBatis, Spring Security, JWT
- MariaDB

---

## 주요 기능

- **회원가입** — ID/PW 유효성 검사, 중복 확인, 주소 검색(Daum Postcode API), 약관 동의
- **로그인** — JWT 인증, Vuex 상태 관리
- **아이디/비밀번호 찾기**
- **망링레 소개** — 망고, 링고, 레고 고양이 소개 페이지
- **상품 목록 / 장바구니**
- **마이페이지** — 비밀번호 확인 후 프로필 설정

---

## 프로젝트 구조

```
mll/
├── pom.xml                            # Maven 설정
├── src/main/java/org/mll/             # Spring Boot 백엔드
│   ├── MllApiApplication.java
│   ├── controller/joinlogin/          # 로그인/회원가입 REST API
│   ├── service/                       # 비즈니스 로직
│   ├── dao/                           # 데이터 접근
│   └── dto/                           # 데이터 전송 객체
├── src/main/resources/
│   ├── application.properties         # DB + JWT 설정
│   └── mapper/                        # MyBatis SQL 매퍼
└── mllfrontend/                       # Vue 3 SPA
    └── src/
        ├── components/main/           # Header, Footer, Home
        ├── components/about/          # 소개, 상품
        ├── components/navbar/         # 로그인, 회원가입, 장바구니, 마이페이지
        ├── router/router.js           # 라우팅 (10개 경로)
        └── Store/store.js             # Vuex 상태 관리
```

---

## 실행 방법

### Backend
```bash
# MariaDB 실행 필요 (port 3311, database: mll_db)
./mvnw spring-boot:run
```

### Frontend
```bash
cd mllfrontend
npm install
npm run serve
```

---

