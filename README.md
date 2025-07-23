# 🎥 Website Project: Movie 306

안녕하세요! Movie 306 프로젝트에 대한 README입니다.

---

## 📅 프로젝트 개요

* **프로젝트명:** Movie 306
* **작업 기간:** 2025.07.02-2025.07.16.

---

## ⏰ 프로젝트 일정

* **기획:** 8시간
* **디자인:** 12시간
* **개발:** 20시간

---

## 📝 목차

1. [프로젝트 개요](#1-프로젝트-개요)  
   1.1. [작업 배경](#11-작업-배경)  
   1.2. [키워드](#12-키워드)  
2. [파일 구성](#2-파일-구성)  
3. [주요 기능 소개](#3-주요-기능-소개)  
   3.1. [메인 페이지](#31-메인-페이지)  
   3.2. [서브 페이지 (총 3개)](#32-서브-페이지-총-4개)  
4. [작업 환경](#4-작업-환경)  
5. [관련 링크](#5-관련-링크)

---

## 1. 프로젝트 개요

### 1.1. 작업 배경

기존 영화 정보 사이트들은 정보가 산재되어 있어
사용자가 원하는 영화를 효율적으로 찾기 어렵고,
디자인 일관성과 콘텐츠 분류 체계가 부족한 경우가 많았습니다.

또한, 영화 상세 정보나 리뷰 확인, 추천 시스템 등이 분산돼 있어
사용자 흐름이 끊기고 몰입감이 떨어지는 문제가 있었습니다.
이번 Movie 306 프로젝트는
영화 검색과 추천 기능을 직관적이고 통합된 구조로 구현하여,
사용자의 탐색 경험을 개선하고자 기획되었습니다.

* 영화 정보를 섹션별(인기, 상영 중, 평점 높은 등)로 정리해 메인 페이지에서 한눈에 파악 가능하도록 구성
* 키워드 검색 기능을 통해 사용자가 원하는 영화를 즉시 찾을 수 있도록 인터페이스 개선
* 영화 상세 페이지에서는 줄거리, 배우, 리뷰, 추천 영화 등 종합 정보 제공으로 몰입도 높은 사용자 경험 제공
* 로그인/마이페이지 기능을 통해 유저 개인화 기반의 확장성 확보
* 전체적으로 어두운 테마와 노란 포인트 컬러를 활용해 감각적인 시네마 무드 연출

👉 기술적으로는 React 기반의 프로젝트로,
**비동기 데이터 관리에 TanStack Query(React Query)**를 사용해
async/await 방식으로 TMDB API 데이터를 가져오고, 캐싱, 로딩 상태, 에러 처리 등을 효율적으로 관리했습니다.

스타일링은 SCSS와 React-Bootstrap을 활용해 커스터마이징했으며,
React 멀티 캐러셀 라이브러리를 통해 인기 영화 섹션 등의 슬라이드를 구현했습니다.
또한, 아이콘은 React-Bootstrap Icons를 사용했고,
Netlify를 통해 배포했으며 404 리디렉션 설정도 직접 구성해 실제 운영 환경을 고려한 배포까지 완료했습니다.

### 1.2. 키워드

* 직관적인 콘텐츠 분류(인기, 상영 중, 평점순, 예정작 등)
* 키워드 기반 검색 기능
* 영화 상세 페이지 내 통합 정보 제공 (배우, 리뷰, 추천 포함)
* 로그인 / 마이페이지 등 사용자 인증 및 개인화 기능
* 감성적이고 몰입감 있는 시네마 무드 UI

---

## 2. 파일 구성
```
🌱 fsip
 ┣ 📂 public
   📄 index.html
   ┗ 📂 image
 ┣ 📂 src
   ┣ 📂 hook
     📄 useGenreList.jsx
     📄 useMovieCredits.jsx
     📄 useMovieDetail.jsx
     📄 useMovieReviews.jsx
     📄 useMovieSimilar.jsx
     📄 useMovieTrailer.jsx
     📄 useNowPlayingMovieQuery.jsx
     📄 usePopularMovies.jsx
     📄 useSearchMovieQuery.jsx
     📄 useTopRatedMoviesQury.jsx
     📄 useUpcomingMoviesQuery.jsx
   ┣ 📂 layouts
     📄 AppLayoout.jsx
   ┣ 📂 pages
     ┣ 📂 homepage
       📄 HomePage.jsx
       ┣ 📂 components / banner
         📄 Banner.jsx
       ┣ 📂 movieCard
         📄 MovieCard.jsx
       ┣ 📂 NowPlayingMovieSlide
         📄 NowPlayingMovieSlide.jsx
       ┣ 📂 PopuularMovieSlide
         📄 PopuularMovieSlide.jsx
       ┣ 📂 TopRatedMoviesSlide
         📄 TopRatedMoviesSlide.jsx
       ┗ 📂 UpcomingMovieSlide
         📄 UpcomingMovieSlide.jsx
     ┣ 📂 mociedetailpage
       📄 MovieDetailPage.jsx
       📄 MovieDetailPage.style.scss
     ┗ 📂 moviepage
       📄 MoviePage.jsx
       📄 MoviePage.style.scss
     📄 Login.jsx
     📄 MyPage.jsx
     📄 NotFoundPage.jsx
   ┣ 📂 styles
     📄 _mixin.scss
     📄 App.scss
     📄 variables.scss
   ┗ 📂 utils
     📄 api.js
   📄 category-main.html
   📄 class-detail.html
   📄 member-register.html
   📄 take-course.html  
 ┣ 📂 css
 ┗ 📂 style
   📄 fonts.scss
   📄 reset.scss
   📄 responsive-mobile.scss
   📄 responsive-tablet.scss
   📄 style.scss
   📄 variables.scss
 


```

   </br>
   </br>
   </br>

---


## 3. 주요 기능 소개

### 3.1. 메인 페이지

<img width="1920" height="2958" alt="image" src="https://github.com/user-attachments/assets/4fa5f9cb-5d05-4755-9e5c-3935c3cfdc99" />




#### 3.1.1. 헤더

<img width="1368" height="58" alt="image" src="https://github.com/user-attachments/assets/f99ec65b-853c-40a4-bcb9-1689c78daaa7" />

<img width="1894" height="890" alt="image" src="https://github.com/user-attachments/assets/8b476d06-0e02-4d34-99d6-1c1c0f27b406" />

* 좌측에는 홈과 메뉴 우측에는 서치박스를 구성하였습니다.
* 서치 박스를 포커스 했을 때 배경에 컬러가 들어가도록 만들었습니다. 
* 서치 박스에 검색했을 때 경고창과 함께 페이지 이동으로 결과가 없다고 뜨도록 만들었습니다.
  

#### 3.1.2. 메인페이지 배너

<img width="1331" height="503" alt="image" src="https://github.com/user-attachments/assets/4f06df40-2986-4bd8-a24e-26d5f757588e" />

<img width="535" height="384" alt="image" src="https://github.com/user-attachments/assets/b9f93324-a960-4dad-ba60-b509692c2540" />

* 제일 인기있는 영화를 불러와 보여주는 배너입니다.
* 뒷배경에  before 값을 활용하여 위에서부터 투명해지는 그라데이션을 넣어 글씨가 더 잘 보이도록 만들었습니다.
* 내용은 row를 활용하여 한 줄로 배치했으며 좌측에는 포스터를, 우측에는 영화에 대한 정보를 불러왔습니다.
* 트레일러 버튼을 클릭했을 때 유튜브에서 영화 트레일러를 불러와 모달로 확인 할 수 있게 제작하였습니다.



#### 3.1.3. 메인페이지 영화소개

<img width="1861" height="894" alt="image" src="https://github.com/user-attachments/assets/93f34879-cd21-4503-be89-01d822111357" />


* 각각 다른 hook을 제작하여 데이터를 불러오고 케러셀을 활용하여 슬라이드될 수 있도록 제작하였습니다.
* 일정 시간이 지나면 자동으로 넘너가도록 제작했으며 마우스 드레그로도 이동이 가능합니다.

  

#### 3.2.1. 서브페이지 영화 디테일

<img width="1920" height="1884" alt="image" src="https://github.com/user-attachments/assets/91133c47-52d3-480c-964a-253b550a0c02" />

* 메인에서 영화를 클릭했을 시 나오는 디테일 페이지입니다.
* 제일 상단은 배너 형태로 제작했으며 메인 페이지와 동일하게 좌측에는 포스터, 우측에는 영화 설명이 나오도록 구성하였습니다.
* 출연배우 부분은 배우들의 정보를 불러와 케러셀을 활용하여 슬라이드 될 수 있도록 제작하였고 사진 밑에는 배우의 극 중 이름과 본명이 나오도록 만들었습니다.
* 영화 리뷰 부분은 좌측에는 작은 프로필 사진이 보이며 우측에는 작성자 이름과 내용, 날짜가 보여집니다.
* 프로필 사진이 만약 없으면 다른 이미지로 대체되도록 제작하였으며 리뷰 내용도 일정 글자 이상이면 잘리도록 만들어 보기 좋게 구성하였습니다.
* 추천 영화 부분도 훅을 만들어 데이터를 불러온 후 캐러셀로 제작해 자동으로 돌아가게 제작하였습니다.



#### 3.2.2. 서브페이지 마이페이지

<img width="1909" height="860" alt="image" src="https://github.com/user-attachments/assets/8ccb9bcd-4f72-4146-ab4c-085288d5e628" />


* 마이페이부분입니다. 좌측에는 본인에 대한 기본정보와 내 정보, 알림함, 공지사항 등 버튼을 제작하였습니다.
* 우측에는 시청내역을 구성하였으며, 찜목록에는 메인에서 사용한 데이터를 불러와 슬라이드로 제작하였습니다.
에 배경으로는 천천히 돌아가는 애니메이션을 적용하여 홈페이지가 심심하지 않도록 만들었습니다.



#### 3.2.3. 서브페이지 로그인페이지

<img width="1903" height="912" alt="image" src="https://github.com/user-attachments/assets/ccf29abc-3630-4a61-a5c7-31ccf6a8a6a2" />

* 로그인 페이지입니다. 좌측에는 로그인에 대한 문구를 작성하고 우측에 로그인에 대한 내용을 박스 형태로 제작하였습니다.
* 306 글자를 뒷 배경으로 사용해 심심해 보이지 않게 구성하였습니다.



#### 3.2.4. 서브페이지 404페이지

<img width="1895" height="880" alt="image" src="https://github.com/user-attachments/assets/25a2d4e2-53f5-4e28-8e71-7a18c59cd8ce" />

* 결과가 없거나 경로가 잘 못 됐을 때 보여지는 페이지입니다. 큰 글씨로 안내문구를 넣었으며 홈으로 가는 버튼을 제작하여 홈으로 돌아갈 수 있도록 만들었습니다.



---

## 4. 작업 환경

### 4.1. 사용 프로그램

* **노션:** 작업 기록
* **피그마:** 기획 및 와이어 프레임, 디자인
* **VS Code**

### 4.2. 사용 언어

* **HTML**
* **SCSS**
* **JavaScript**
* **React**

### 4.3. 작업 해상도

* **PC 기준:** 1920x1080
* **PC 기준:** 3440x1440
* **반응형 대응:** 768px

### 4.4. 윈도우 버전

* **Window 10**
* **Window 11**

---

## 5. 관련 링크

* [프로젝트 GitHub Repository] https://github.com/hyohee22/Movie.git
* [배포된 웹사이트 링크] https://coruscating-palmier-1f4905.netlify.app/
