# HTML 이해하기
---
# 📖목차
  - [HTML 정의](#html-정의)
  - [HTML 문법](#html-문법)
  - [HTML 문법 -> 태그](#html-문법-태그)
  - [HTML 문법 -> 속성](#html-문법-속성)
  - [HTML 문법 -> 태그 중첩](#html-문법-태그-중첩)
  - HTML 문법 -> 빈 태그
  - HTML 문법 -> 공백
  - HTML 문법 -> 주석
  - 문서의 기본 구조
<br>
  
---
<br>
  
## HTML 정의
  - 웹페이지를 만드는 언어
  - Hyper Text = 링크
  - Markup Language : 프로그래밍 언어의 한 종류로 정보를 구조적, 계층적으로 표현 가능
  - 확장자 .html
<br>

## HTML 문법
  1. 태그
  2. 속성
  3. 태그 중첩
  4. 빈태그
  5. 공백
  6. 주석
<br>

## HTML 문법 (태그)
> 태그란? 무언가를 표시하기 위한 꼬리표 or 이름표<br>
> 요소란? 내용을 포함한 태그 전체를 요소라고 한다.

- 태그는 기호 <,>로 표현하고, 사이에 태그 이름이 주어진다.
- 시작태그`<태그명>`와 종료태그`</태그명>`로 이루어져 있다. (종료태그엔 이름 앞에 `/`기호가 붙는다.
- 시작태그와 종료태그 사이에는 실제 화면에 나타나는 내용이 위치한다.

### HTML 예제 code
```html
<h1> Hello,HTML</h1>
```
<h1> Hello,HTML</h1>

[🚀위로 가기](#목차)
<br><br>

## HTML 문법 (속성)
> 속성이란? 태그에 추가로 정보를 제공하거나 태그의 동작이나 표현을 제어할 수 있는 설정 값

- 속성은 이름과 값으로 이루어져 있다.
- 시작 태그에서 태그 이름 뒤 공백으로 구분 후 `속성 이름="속성값"`으로 표현한다.
- 속성 값은 ''와 ""로 감싸 표현한다.
- 의미와 용도에 따라 여러 속성이 존재하며 하나의 태그에 여러 속성을 선언할 수 있다.
- 속성의 종류
  - 모든 태그에 사용할 수 있는 속성(글로벌 속성) or 특정 태그에만 사용할 수 있는 속성
  - 선택적으로 사용 가능한 속성 or 특정 태그에서 필요한 필수 속성 
<br>

### 1. id와 class 2개의 속성을 이용한 예제
```html
<h1 id="title" class="main">Hello,HTML</h1>
```
<h1 id="title" class="main">Hello,HTML</h1>
<br>

### 2. img태그에 src속성을 이용한 예시 
```html
<h1>Hello,HTML</h1>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/120px-HTML5_logo_and_wordmark.svg.png" width="50%">
```
<h1>Hello,HTML</h1>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/120px-HTML5_logo_and_wordmark.svg.png" width="10%">

[🚀위로 가기](#목차)
<br><br>

## HTML 문법 (태그 중첩)
