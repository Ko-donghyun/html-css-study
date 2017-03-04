
    ██╗  ██╗████████╗███╗   ███╗██╗          ██████╗███████╗███████╗
    ██║  ██║╚══██╔══╝████╗ ████║██║         ██╔════╝██╔════╝██╔════╝
    ███████║   ██║   ██╔████╔██║██║         ██║     ███████╗███████╗
    ██╔══██║   ██║   ██║╚██╔╝██║██║         ██║     ╚════██║╚════██║
    ██║  ██║   ██║   ██║ ╚═╝ ██║███████╗    ╚██████╗███████║███████║
    ╚═╝  ╚═╝   ╚═╝   ╚═╝     ╚═╝╚══════╝     ╚═════╝╚══════╝╚══════╝
                                                                    
                                                              
  --------------------------------------------------------------------

# HTML CSS 스터디

- 기본 환경
  - HMTL5, CSS3

- HTML
  - 문서 기본 틀 잡기
  - 웹 사이트의 내용을 나열
  - HTML 스터디
    - 미리 약속된 태그를 배우는 것
    - 태그를 사용해서 HTML문서를 작성하는 것
  - 태그, 요소, 속성
    - 태그 : h1 태그
    - 요소 : `<h1></h1>`
    - 속성 : 태그 안에 들어가는 정보`<img src='' alt=''/>`
  - 중요 키워드
    - 웹 접근성
      - 어느 부분이 제목인지, 본문인지 정확하게 알 수 있도록 작성되어야 제대로 보인다.
      - 웹 표준에 맞게 작성된 웹 문서라면 키보드만으로 완벽하게 문서 안의 내용 사이를 이동할 수 있다.
      - 검색엔진에서 잘 검색되고, 개발 시간이 단축된다.
      - 내용을 눈으로 확인할 수 없는 시각장애인이든, 마우스를 자유롭게 사용할 수 없는 지체장애인이든 누구나 웹에 있는 콘텐츠를 구애받지 않고 사용할 수 있도록 제작해야 한다는 것
    - 시멘틱(sementic) : 의미있는 태그 사용
      - 인터넷상의 문서들을 보면 큰 구조는 어느정도 비슷하다.
      - 태그만 보고도 어느 부분이 제목이고 메뉴인지 내용인지 쉽게 알 수 있음.
      - 웹 접근성을 높일 수 있음.
      - `<div></div>`태그랑 다를바 없음. 단순 의미 부여를 위해서 사용
      - `<a></a>`태그와 `<button></button>`태그의 차이!
      - 종류
        - 헤더(header) : 사이트의 제목과 로고, 검색 창
        - 네비(nav) : 메뉴를 나타내는 태그, 같은 사이트 안의 문서나 다른 사이트의 문서로 연결하는 링크들
        - 섹션(section) : 콘텐츠 영역 나타내기
        - 아티클(article) : 실제 콘텐츠 내용 넣기
        - 기타(aside) : 본문 이외의 내용 표시
        - 푸터(footer) : 저작권 정보와 제작자 정보를 표시하는 부분
        - 주소(address) : footer 태그 안에 사이트 제작자 정보, 연락처 정보 표시
      - 시멘틱 태그 안에는 타이틀을 나타낼 heading 태그(h1을 제외한)를 넣어야 함
  - !!주의!!
    - `<center>, <b>, <i>, <big>, <frame>`등의 스타일을 나타내는 태그 쓰지 말 것!
    - 인라인 태그(선, 흐름) 안에 블록 태그(면, 영역) 넣지 말 것! `<a></a>`태그는 제외
    - lang 속성 'en', 'ko'을 꼭 넣어줄 것!
    - `<h1></h1>` 태그는 페이지당 딱 한개만 사용할 것!
    - `<img>` 태그에 alt 속성 넣기!
  - 기본 구조
```    
    <!doctype html> <!-- HTML5로 작성하는 문서 -->
    <html lang="ko">
      <head>
        * 문서와 관련된 정보들 나열(언어, 타이틀, 키워드 등)
        <meta> 웹 페이지에 추가 정보를 전달
        <title> 웹 페이지의 제목
        <script> 웹 페이지에 스크립트를 추가
        <link> 웹 페이지에 다른 파일을 추가
      </head>
      <body>
        화면에서 보이는 부분
      </body>
    </html>
```

- CSS
  - 문서 꾸미기
  - 웹 문서의 디자인을 구성
  - [브라우저별 버전별 적용이 가능한 스타일이 다름](http://caniuse.com/#search=flexbox)
  - 반응형 작업시 %로 하고, 모바일 뷰에서 먼저 시작
  - 중요 키워드
    - CSS reset : 기본적인 CSS리셋
      - ress.css
      - normalize.css
    - 박스모델
      - box-size
        - content : 내용
        - padding : 내용과 경계 안쪽 공간
        - border : 경계
        - margin : 경계 외부 바깥쪽 공간
      - display
        - inline : 선
          - float을 알고 있음 > 글자가 이미지를 겹치고 싶지 않다는 생각에서 출발
        - block : 면
          - default height : 자식의 height 
          - default width : 부모의 width
          - default margin : 부모의 width와 연관
    - float : 집 나간 자식
      - clear: both - float 없애기
      - 가상 엘리먼트 - ::after, ::before
        - `.float-contained-div::after {`
        - `  content: ''; // 컨텐트가 없으면 적용되지 않음`
        - `  display: block;`
        - `  clear: both;`
        - `}`
    - position
      - float와 비슷하나 성능상 좋지 않음
      - 종류
        - static : default 설정
        - relative : 본인의 위치는 알고 있음
        - absolute : 본인의 위치를 모름, 기준점(static이 아닌 부모)이 있어야 한다.
        - fixed : 기준이 viewport(브라우저 창 크기)
      - offset
        - top, left (좌상)
        - bottom, right(우하)
    - 플렉스박스(FlexBox) : IE 9 이하는 지원 안된대~
      - [N 스크린](https://material.io/devices/) 대응
      - 가로 정렬, 세로 정렬
      - 실습
        - 1) 부모에게 display: flex로 준다
        - 2) 정렬할 방향 설정
          - 가로 : `flex-direction: row;` (가로 main axis 생성, 세로 cross axis 생성)
          - 세로 : `flex-direction: column;` (세로 main axis 생성, 가로 cross axis 생성)
        - 3) 넘치게 할 것이냐 아니냐
          - `flex-wrap: wrap`
          - `flex-wrap: no-wrap`
        - 추가
          - 위치시키고 싶은 아이템의 속성
            - justify-content : 정방향 정렬
            - align-items : 역방향 정렬
            - align-content
            - align-self
            - order : `flex-child:nth-child(1) { order: 2 }`
          - 위치시키고 싶은 값
            - flex-start
            - flex-end
            - space-between
            - space-around
            - center
  - !!주의!!
    - 직접 스타일을 주지 말 것!
    - 태그 < 클래스 < ID - 주로 클래스로 처리.

- 반응형
  - 주로 글자 크기, 이미지 크기, 위치 정도의 수정
  - meta 태그를 사용하여 화면 너비에 대한 정보를 제공해야 함
    - `<meta name='viewport' content='width=device-width'>`
  - 미디어 쿼리
    - 화면 너비 관련
      - 화면 너비 0픽셀 ~ 767픽셀
        - `@media screen and (max-width: 767px) {}`
      - 화면 너비 768픽셀(아이패드) ~ 959픽셀
        - `@media screen and (min-width: 768px) and (max-width: 959px) {}`
      - 화면 너비 960픽셀(일반 웹) ~
        - `@media screen and (min-width: 960px) {}`
    - 화면 방향 관련
      - 수직
        - `@media screen and (orientation: portrait) {}`
      - 수평
        - `@media screen and (orientation: landscape) {}`
    - 레티나(고해상도)
      - `@media screen and (-webkit-min-device-pixel-ratio: 2) {}`
  - 그리드 시스템
    - 반응형 웹은 대부분 그리드 시스템을 사용
    - [부트스트랩](http://getbootstrap.com/css/#grid)에도 존재
    - 
  
- 참고
  - 멋쟁이 사자처럼 5기 겨울 방학 스터디(서강대 멋사 운영진 노지승님)
  - 모던 웹 디자인을 위한 HTML5+CSS3 입문 책
  - 