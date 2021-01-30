# HTML 이해하기
---
# 📖목차
  - [HTML 정의](#html-정의)
  - [HTML 문법](#html-문법)
  - [HTML 문법 -> 태그](#html-문법-태그)
  - [HTML 문법 -> 속성](#html-문법-속성)
  - [HTML 문법 -> 태그 중첩](#html-문법-태그-중첩)
  - [HTML 문법 -> 빈 태그](#html-문법-빈-태그)
  - [HTML 문법 -> 공백](#html-문법-공백)
  - [HTML 문법 -> 주석](#html-문법-주석)
  - [문서의 기본 구조](#문서의-기본-구조)
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
> 태그 중첩이란? 태그 안에 다른 태그를 선언할 수 있다. (태그를 중첩해서 사용시 중첩되는 태그는 부모 태그를 벗어나서는 안된다.)

### 올바른 태그 중첩 예시 
```html
<h1> hello,<i>HTML</i></h1>
```
<h1> hello,<i>HTML</i></h1>

### 잘못된 태그 중첩 예시 
```html
<h1> hello,<i>HTML</h1></i>
```

[🚀위로 가기](#목차)
<br><br>

## HTML 문법 (빈 태그)
> 빈 태그란? 일반적인 태그와 달리 내용이 없어 종료 태그가 없다. 
- 빈 태그 특징: 내용만 비어있을 뿐 속성을 통해 화면에 나타내거나 표시되지 않더라도 다른 용도로 사용된다. ex) 텍스트 강조

[🚀위로 가기](#목차)
<br><br>

## HTML 문법 (공백)
> HTML은 두 칸 이상의 공백을 모두 무시한다.(공백처리 방식에 대해서 CSS로 제어 가능)

### 세가지 모두 같은 텍스트가 나오는 예시(두 칸 이상의 공백과 개행을 모두 무시)
```html
<h1>Hello, HTML</h1>
<h1>Hello,     HTML</h1>
<h1>
    Hello,
    HTML
</h1>
```
<h1>Hello, HTML</h1>
<h1>Hello,     HTML</h1>
<h1>
    Hello,
    HTML
</h1>

[🚀위로 가기](#목차)
<br><br>

## HTML 문법 (주석)
> 주석은 화면에 노출되지 않고 메모의 목적으로만 사용하는 것을 의미
HTML 파일 내에서 주석 표시를 해주면 브라우저는 해당 부분을 인식하여 해석하지 않는다. `<!--내용-->`

### 주석 처리 예시
```html
<!-- 여기에 작성되는 내용들은 모두 주석 처리가 됩니다. -->
<!-- 주석은 여러 줄로 작성할 수도 있습니다.
    <h1>Hello, HTML</h1>
    위 <h1>태그는 브라우저가 해석하지 않습니다.
-->
```
[🚀위로 가기](#목차)
<br><br>

## 문서의 기본 구조
> 문서의 구조란? 웹 페이지를 만들기 위한 가장 기본이 되는 정보로써 브라우저는 HTML 문서 구조를 통해 HTML의 정보를 파악한다.

### HTML의 기본구조: 웹 문서를 작성할 때 반드시 들어가야하는 기본적인 내용으로 문서 타입 정의와 <html>요소로 나뉜다.
  
```html
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <h1>Hello, HTML</h1>
    </body>
</html>
```
  
1. 문서 타입 정의: 문서 타입 정의: 해당 문서가 어떤 버전으로 작성되었는지 브라우저에 알려주는 선언문이며 반드시 문서 내 최상단에 선언 `<!DOCTYPE html>`
2. `<html>` 요소
  - `부모 태그: <html>` `자식 태그: <head>, <body>`
  - `<html>의 lang 속성`: 문서 작성 언어
  - `<head>`: 문서의 기본 정보 설정이나 외부 스타일 시트 파일 및 js파일을 연결하는 등의 역할(화면에 표시되진 않음)
  - `<meta>의 charset 속성`: 문자의 인코딩 방식을 지정
  - `<title>`: 검색 엔진이 웹 페이지를 분석할 때 가장 중요하게 생각하는 태그
  - `<body>`: 실제 브라우저 화면에 나타나는 내용이 들어간다.(본문 태그)
  
### 예시

```html
<!doctype html>
<html>
<head>
  <title>WEB1 - html</title>
  <meta charset="utf-8">
</head>
<body>
  <ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
  </ol>
  <h1>HTML</h1>
  <p>Hypertext Markup Language (HTML) is the standard markup language for <strong>creating <u>web</u> pages</strong> and web applications.Web browsers receive HTML documents from a web server or from local storage and render them into multimedia web pages. HTML describes the structure of a web page semantically and originally included cues for the appearance of the document.
  <br><img src="https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3135/7648.png" width="30%">
  </p><p style="margin-top:10px;">HTML elements are the building blocks of HTML pages. With HTML constructs, images and other objects, such as interactive forms, may be embedded into the rendered page. It provides a means to create structured documents by denoting structural semantics for text such as headings, paragraphs, lists, links, quotes and other items. HTML elements are delineated by tags, written using angle brackets.
  </p>
</body>
</html> 
```

<body>
  <ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
  </ol>
  <h1>HTML</h1>
  <p>Hypertext Markup Language (HTML) is the standard markup language for <strong>creating <u>web</u> pages</strong> and web applications.Web browsers receive HTML documents from a web server or from local storage and render them into multimedia web pages. HTML describes the structure of a web page semantically and originally included cues for the appearance of the document.
  <br><img src="https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3135/7648.png" width="30%">
  </p><p style="margin-top:10px;">HTML elements are the building blocks of HTML pages. With HTML constructs, images and other objects, such as interactive forms, may be embedded into the rendered page. It provides a means to create structured documents by denoting structural semantics for text such as headings, paragraphs, lists, links, quotes and other items. HTML elements are delineated by tags, written using angle brackets.
  </p>
</body>

> 예제는 body만 출력한다.

[🚀위로 가기](#목차)
