# 내일의 집

오늘의 집 웹페이지를 모티브로하여 김버그 강의를 참고로 진행하였습니다.

3차 프로젝트에서 디자이너 분과 협업 후 부족했던 부분을 보강하고자 시작하였습니다.

## (Grid System) Web
![내일의집_시연2](https://user-images.githubusercontent.com/77766718/141097875-315039fc-973f-410c-94c7-302e81f5a211.gif)

## App
<img width="366" alt="스크린샷 2021-11-10 오후 8 14 39" src="https://user-images.githubusercontent.com/77766718/141103629-9ab16783-d0e3-44cc-9284-739fec339739.png">

### 구현 단계
+ UI : 모바일,테블릿,데스크탑
- [x] Header
- [x] NavBar
- [x] 목록 페이지
- [x] 카테고리
- [x] 검색 페이지
- [x] 제품 상세페이지
- [x] Footer

### 대표적인 구현
1. Grid System을 이용한 반응형 웹페이지 (모바일, 테블릿, 데스크탑)

2. 공통 디자인 module 관리 (재사용 가능한 css 구축)
+ Text-Style(size,color)
+ Typography (font-height, font-weigth, letter-spacing, font-family etc..)
+ @mixin
  + Responsive(모바일,테블릿,데스크탑)
  + Positions
  + FlexBox
  $flex-map: (
  start: flex-start,
  end: flex-end,
  between: space-between,
  around: space-around,
  stretch: stretch,
  center: center,
); 

3. 기기에 맞는 디자인 변화
4. Carousel 제품 상세페이지


<img width="241" src="https://user-images.githubusercontent.com/77766718/137096199-1980c87a-989a-4cc1-a6dd-3cbcfa1f7542.png"> <img width="239" src="https://user-images.githubusercontent.com/77766718/137096244-b1e9e66a-ffdf-4b1d-9689-9c01594b684c.png">





### 1. GNB

- 로그인 하지 않은 경우

```html
<div class="button-group">
  <button
    class="gnb-icon-button is-search lg-hidden"
    type="button"
    aria-label="검색창 열기 버튼"
  >
    <i class="ic-search"></i>
  </button>

  <a
    class="gnb-icon-button is-cart"
    href="/"
    aria-label="장바구니 페이지로 이동"
  >
    <i class="ic-cart"></i>
  </a>

  <div class="gnb-auth sm-hidden">
    <a href="">로그인</a>
    <a href="">회원가입</a>
  </div>
</div>
```

- 로그인을 했을 경우

```html
<div class="button-group">
  <button
    class="gnb-icon-button is-search lg-hidden"
    type="button"
    aria-label="검색창 열기 버튼"
  >
    <i class="ic-search"></i>
  </button>

  <a
    class="gnb-icon-button sm-hidden"
    href="/"
    aria-label="스크랩북 페이지로 이동"
  >
    <i class="ic-bookmark"></i>
  </a>

  <a
    class="gnb-icon-button sm-hidden"
    href="/"
    aria-label="내소식 페이지로 이동"
  >
    <i class="ic-bell"></i>
  </a>

  <a
    class="gnb-icon-button is-cart"
    href="/"
    aria-label="장바구니 페이지로 이동"
  >
    <i class="ic-cart"></i>
    <strong class="badge">92</strong>
  </a>

  <button
    class="gnb-avatar-button sm-hidden"
    type="button"
    aria-label="마이메뉴 열기 버튼"
  >
    <div class="avatar_32">
      <img src="/assets/images/img-user-01.jpg" alt="사달라 아저씨" />
    </div>
  </button>
</div>
```

### 2. Sidebar

- 로그인 하지 않은 경우

```html
<div class="sidebar-auth">
  <a class="btn-outlined btn-40" href="/">로그인</a>
  <a class="btn-primary btn-40" href="/">회원가입 </a>
</div>
```

- 로그인을 했을 경우

```html
<div class="sidebar-user">
  <a href="/">
    <div class="avatar_24">
      <img src="/assets/images/img-user-01.jpg" alt="사달라 아저씨" />
    </div>
    <strong class="username">사달라사달라사달라사달라</strong>
  </a>
</div>
```
