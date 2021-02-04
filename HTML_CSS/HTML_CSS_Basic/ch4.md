# CSS 이해하기
---
# 📖목차
  - [CSS 소개](#CSS-소개)
  - [CSS 문법과 적용](#CSS-문법과-적용)
  - [선택자1](#선택자1)
  - [선택자2](#선택자2)
  - [선택자3](#선택자3)
  - [문서 구조 관련 선택자](#문서-구조-관련-선택자)
  - [가상 선택자1](#가상-선택자1)
  - [가상 선택자2](#가상-선택자2)
  - [구체성](#구체성)
  - [상속](#상속)
  - [캐스캐이딩](#캐스캐이딩)
<br>
  
---
<br>
  
## CSS 소개
> HTML을 꾸며주는 언어로, HTML을 보기 좋게 디자인하는 역할 (독립적으로 사용 불가능)<br>

[CSS 디자인 참고](http://www.csszengarden.com/)
> 같은 HTML을 사용하지만 CSS를 다르게 하여 다른 디자인을 만들어냄

[🚀위로 가기](#목차)
<br><br>

## CSS 문법과 적용
```css
h1 {color: yellow; font-size: 2em;}
```
- 예시 
  - `선택자(어느 요소를 꾸밀건지 선택)`: h1
  - `속성`: color, font-size
  - `값`: yellow, 2em
  - `선언`: color: yellow; font-size: 2em;
  - `선언부`: {color: yellow; font-size: 2em;}
  - `규칙(선언끼리는 개행 가능)`: h1 {color: yellow; font-size: 2em;} 

- CSS 적용방식
1. `Inline`: 해당 요소에 직접 스타일 속성을 이용해 규칙들을 선언하는 방법으로, 선택자가 필요없고 선언부에 내용만 스타일 속성의 값으로 넣어준다.
```html
<div style="color: red;"> 내용</div>
```

2. `Internal`: head 내부에 style을 선언하고 안에 규칙을 넣는다.
```html
<!--div 태그=빨간색-->
<style> div {color: red;} </style>
```

3. `External`: 스타일 규칙들을 별도의 외부 파일에 만들어 시트 파일을 이용한다  (파일명.css)
```css
/*Red.css*/
div {color: red;}
```
```html
<link rel="stylesheet" href="Red.css">
```
> head내부에 link를 선언후 href를 통해 파일 경로를 적는다 (css파일은 stylesheet)<br>
> 수정이 필요한 경우 css 파일을 수정하면 모든 페이지에 반영 가능.

4. `Import`: 스타일 시트내에서 다른 스타일 시트를 불러오는 방식 (거의 사용 x)

[🚀위로 가기](#목차)
<br><br>

## 선택자1
> 복잡하고 다양한 요소들 사이에 내가 원하는 요소만을 선택할 수 있도록 도와준다.

- 요소 선택자
  - 선택자 중에 가장 기본이 되는 선택자이며 `태그 선택자`라고도 한다.
```css
h1 { color: yellow; }
h2 { color: yellow; }
h3 { color: yellow; }
h4 { color: yellow; }
h5 { color: yellow; }
h6 { color: yellow; }
```
> 선택자 부분에 태그 이름이 들어가, 문서내에 선택자에 해당하는 모든 요소에 스타일 규칙 적용

- 그룹화
> 선택자는 쉼표를 통해 그룹화 가능
```css
h1, h2, h3, h4, h5, h6 { color: yellow; } /*선택자 그룹화*/
* { color: yellow; } /*전체 선택자*/
h1 { color: yellow; font-size: 2em; background-color: gray; } /*선언 그룹화*/
h1, h2, h3, h4, h5, h6 { color: yellow; font-size: 2em; background-color: gray; } /*선택자, 선언 그룹화*/
```

[🚀위로 가기](#목차)
<br><br>

## 선택자2

- Class 선택자
> 요소에 구애받지 않고 스타일 규칙을 정용할 수 있는 방법중 하나.<br>
> class 선택자를 사용하기 위해 class 속성을 추가.

```css
.html { color: purple; }
.css { text-decoration: underline; }
/*class 선택자를 사용할 때 선택자명 앞에 .를 찍어준다.*/
```
```html
<dl>
    <dt class="html">HTML</dt>
    <dd><span class="html">HTML</span>은 문서의 구조를 나타냅니다.</dd>
    <dt class="css">CSS</dt>
    <dd><span class="css">CSS</span>는 문서의 표현을 나타냅니다.</dd>
</dl>
```

- 다중 Class
>class 속성은 공백으로 구분해 여러 개의 class를 넣을 수 있다.
```css
.foo { font-size: 30px; }
.bar { color: blue; }
```
```html
<!-- foo와 bar 클래스 적용-->
<p class="foo bar"> ... </p>
```

- id 선택자
> class 선택자와 비슷하지만 .대신 #기호를 사용. 요소에는 id 속성을 쓴다.
```css
#bar { background-color: yellow; }
```
```html
<p id="bar"> ... </p>
```

#### class선택자와의 차이점
  1. #기호 사용
  2. 태그의 class속성이 아닌 id 속성을 참조
  3. 문서 내에 유일한 요소에 사용( id 선택자로 규칙을 적용할 수 있는 요소는 단 하나 이다.)
  4. 구체성

[🚀위로 가기](#목차)
<br><br>

## 선택자3

- 선택자의 조합
```css
p.bar { ... }
/*요소와 class*/
/*<p>이면서 class 속성에 bar가 있어야 적용된다.*/
```
```css
.foo.bar { ... } 
/*class와 class*/
/*class 속성에 foo와 bar가 있어야 적용된다.*/
```
```css
#foo.bar { ... } 
/*id와 class*/
/*id가 foo이며 class가 bar인 요소에 적용된다.*/
```

- 속성 선택자
```html
<p class="foo">Hello</p>
<p class="bar">CSS</p>
<p class="baz" id="title">HTML</p> 
```

1. 단순 속성으로 선택
```css
p[class] { color: silver; } 
/*p이면서 class속성이 있는 요소이면 적용 1, 2, 3 모두 적용*/

p[class][id] { text-decoration: underline; } 
/*p이면서 class속성과 id속성이 있는 요소면 적용 3만 적용*/
```
2. 정확한 속성 값으로 선택
```css
p[class="foo"] { color: silver; } 
/*<p>이면서 class속성의 값이 foo일 때 적용 1만 적용*/

p[id="title"] { text-decoration: underline; }
/*<p>이면서 id속성의 값이 title일 때 적용 3만 적용*/
```
3. 부분 속성 값으로 선택
> 부분 속성값으로 선택은 속성 이름과 속성값 사이에 사용되는 기호에 따라 동작이 조금 다르다. 
#### 부분 속성 값 분류
- [class~="bar"] : class 속성의 값이 공백으로 구분한 "bar" 단어가 포함되는 요소 선택
- [class^="bar"] : class 속성의 값이 "bar"로 시작하는 요소 선택
- [class$="bar"] : class 속성의 값이 "bar"로 끝나는 요소 선택
- [class*="bar"] : class 속성의 값이 "bar" 문자가 포함되는 요소 선택

```html
<p class="color hot">red</p>
<p class="cool color">blue</p>
<p class="colorful nature">rainbow</p>
```

```css
p[class~="color"] { font-style: italic; } /* 1, 2번째 요소 */
p[class^="color"] { font-style: italic; } /* 1, 3번째 요소 */
p[class$="color"] { font-style: italic; } /* 2번째 요소 */
p[class*="color"] { font-style: italic; } /* 1, 2, 3번째 요소 */
```
[🚀위로 가기](#목차)
<br><br>

## 문서 구조 관련 선택자

[🚀위로 가기](#목차)
<br><br>

## 가상 선택자1

[🚀위로 가기](#목차)
<br><br>

## 가상 선택자2

[🚀위로 가기](#목차)
<br><br>

## 구체성

[🚀위로 가기](#목차)
<br><br>

## 상속

[🚀위로 가기](#목차)
<br><br>

## 캐스캐이딩

[🚀위로 가기](#목차)
<br><br>
