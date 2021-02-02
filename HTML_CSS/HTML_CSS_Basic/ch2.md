# HTML 태그
---
# 📖목차
  - [제목과 단락요소](#제목과-단락요소)
  - [텍스트를 꾸며주는 요소](#텍스트를-꾸며주는-요소)
  - [앵커 요소](#앵커-요소)
  - [의미가 없는 컨테이너 요소](#의미가-없는-컨테이너-요소)
  - [리스트 요소](#리스트-요소)
  - [이미지 요소](#이미지-요소)
  - [테이블 요소](#테이블-요소)
  - [폼 요소](#폼-요소)
  <br>
  
---
<br>

## 제목과 단락요소<br>
1. **heading 태그(h1~h6)** `<h1>제목</h1>`<br>
   - 문서 내 제목을 표현할 때 사용하는 태그
   - `<h1>~<h6>`까지 숫자가 커질수록 크기가 커진다.
   - 제목 태그를 사용하면 일반 텍스트보다 좀 더 강조되는 스타일 적용
   <br>
   
2. **paragraph 태그(p)** `<p>문단</p>`<br>
   - 단락을 구분해준다.
   - 화면에 별다른 변화는 없지만, 이전보다 훨씬 의미에 맞게 짜인 마크업 구조.
   - `<p>문단</p>`을 통해 단락을 나눈다.
   <br>
   
3. **linebreak 태그(br)** `<br>`<br>
   - <p>: 내부에서 임의로 개행을 하기 위해 사용.(html은 한 칸 이상의 공백 및 개행을 무시하기 때문에.)
   - 닫기 태그와 내용이 존재하지 않는 빈 태그로, 개행 태그이다.
  <br>

### 예제
```html
<h1>역사</h1>
<h2>개발</h2>
<p>
    1980년, 유럽 입자 물리 연구소(CERN)의 계약자였었던 물리학자 팀 버너스리가 HTML의 원형인 인콰이어를 제안하였다.
    <br>... 이하 생략
</p>
<h2>최초 규격</h2>
<p>
    HTML 최초의 일반 공개 설명은 1991년 말에 버너스리가 처음으로 인터넷에서 문서를 "HTML 태그"(HTML tag)로 부르면서 시작되었다.
    ... 이하 생략
</p>
```
<h1>역사</h1>
<h2>개발</h2>
<p>
    1980년, 유럽 입자 물리 연구소(CERN)의 계약자였었던 물리학자 팀 버너스리가 HTML의 원형인 인콰이어를 제안하였다.
    <br>... 이하 생략
</p>
<h2>최초 규격</h2>
<p>
    HTML 최초의 일반 공개 설명은 1991년 말에 버너스리가 처음으로 인터넷에서 문서를 "HTML 태그"(HTML tag)로 부르면서 시작되었다.
    ... 이하 생략
</p><br>

[🚀위로 가기](#목차)
<br><br>

## 텍스트를 꾸며주는 요소
- `<b></b>`: 글자를 굵게 표현하는 태그
- `<i></i>`: 글자를 기울여서 표현하는 태그
- `<u></u>`: 글자의 밑줄을 표현하는 태그
- `<s></s>`: 글자의 중간선을 표현하는 태그

### 예제
```html
<p>
    <b>Lorem</b> <i>ipsum</i> dolor sit amet<br>
    <u>Lorem</u> <s>ipsum</s> dolor sit amet
</p>
```
<p>
    <b>Lorem</b> <i>ipsum</i> dolor sit amet<br>
    <u>Lorem</u> <s>ipsum</s> dolor sit amet
</p><br>

[🚀위로 가기](#목차)
<br><br>

## 앵커 요소
> 앵커 태그란? HTML에서 HT는 링크를 의미한다. 이때 앵커 태그는 이런 링크를 생성하여 다른 페이지로 이동하거나 현재 페이지 내에서 특정 위치로 초점을 이동시킨다.

```html
<a href="http://www.naver.com/" target="_blank">네이버</a>
```

- `<a></a>`: 앵커 태그  
- `href 속성`: 링크의 목적지가 되는 URL
- `target 속성`: 링크된 리소스를 어디에 표시할지 나타내는 속성
  - `_self`: 현재 화면에 표시. default 값.
  - `_blank`: 새로운 창에 표시. 즉, 외부 페이지가 나타나게끔 하는 속성
  - `_parent`, `_top`: 프레임이라는 특정 조건에서 사용하는 속성
- [기타 속성 참고 자료](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)
<br>

```html
<a href="#some-element-id">회사 소개로 이동하기</a>
... 중략.
<h1 id="some-element-id">회사 소개</h1>
```
- 내부 링크: 앵커 태그를 통해 페이지 내부의 특정 요소로 초점을 이동(내부 링크)
  - `href="#요소-id"`<br>

[🚀위로 가기](#목차)
<br><br>

## 의미가 없는 컨테이너 요소
> 태그 자체에 아무 의미가 없고 단순히 요소를 묶기 위해 사용하는 태그<br>
> 스타일을 주거나 서버에 보내는 데이터를 담기 위한 용도로 사용
- `<div></div>`: 블록 레벨 태그 (한 줄에 하나의 요소)
- `<span></span>`: 인라인 레벨 태그 (한 줄에 여러개의 요소)
- `<p>`: 블록 레벨 태그 , `<b>, <i>, <u>, <s>`: 인라인 레벨 태그<br>

[🚀위로 가기](#목차)
<br><br>

## 리스트 요소
- `<ul>`: 순서가 없는 리스트를 표현 (unorderd list)
- `<ol>`: 순서가 있는 리스트를 표현 (ordered list)
  - `<li>`: 리스트 내 항목을 선언할 때 사용
- `<dl>`: 정의 리스트를 표현
  - `<dt>`: 용어
  - `<dd>`: 용어에 대한 설명
  
### 예제
```html
<ul>
  <li> 사자</li>
  <li> 호랑이</li>
</ul>
<ol>
  <li> 물 넣고 끓이기</li>
  <li> 면,스프 넣기</li>
</ol>
<dl>
  <dt>연필</dt> 
  <dd>글씨를 쓰는데 필요한 물건</dd>
  <dt>지우개</dt> 
  <dd>글씨를 지우는데 필요한 물건</dd>
</dl>
```

<ul>
  <li> 사자</li>
  <li> 호랑이</li>
</ul>
<ol>
  <li> 물 넣고 끓이기</li>
  <li> 면,스프 넣기</li>
</ol>
<dl>
  <dt>연필</dt> 
  <dd>글씨를 쓰는데 필요한 물건</dd>
  <dt>지우개</dt> 
  <dd>글씨를 지우는데 필요한 물건</dd>
</dl><br>

[🚀위로 가기](#목차)
<br><br>

## 이미지 요소

### 예제

```html
<img src="https://cdn.dominos.co.kr/admin/upload/goods/20200311_x8StB1t3.jpg" width="20%" height="40%" alt="피자">
```
<img src="https://cdn.dominos.co.kr/admin/upload/goods/20200311_x8StB1t3.jpg" width="20%" height="40%" alt="피자">

- `<img>`: 문서에 이미지를 삽입하는 태그 (self closing tag)
   - `src 속성`: 이미지 태그의 필수 속성. 경로를 나타내는 속성
   - `alt 속성`: 이미지의 대체 텍스트를 나타내는 속성(이미지를 나타내는 글)
   - `width/height 속성`: 이미지의 가로/세로 크기를 나타내는 속성. (default: 원본크기, 둘중 하나만 선언시 자동 비율 조정)
  
- `상대 경로`: 현재 웹페이지를 기준으로 이미지의 위치를 나타내는 경로
- `절대 경로`: 실제 이미지가 위치한 곳의 주소<br>

[🚀위로 가기](#목차)
<br><br>

## 테이블 요소

### 표의 구성요소
- `<table></table>`: 표를 나타낸다.
  - `<tr></tr>`: 행을 나타낸다.
  - `<th></th>`: (제목)셀을 나타낸다.
  - `<td></td>`: (내용)셀을 나타낸다.
    - `colspan="숫자"`: 숫자만큼의 열을 병합한다.
    - `rowspan="숫자"`: 숫자만큼의 행을 병합한다.
- 하나의 `<table>`은 하나 이상의 `<tr>`로 이루어져있고, `<tr>`은 셀을 나타내는 `<th>,<td>`를 자식으로 가진다. 

### 표의 구조와 관련된 태그
- `<caption></caption>`: 표의 제목을 나타내는 태그
- `<thead></thead>`: 제목 행을 그룹화하는 태그
- `<tfoot></tfoot>`: 바닥 행을 그룹화하는 태그
- `<tbody></tbody>`: 본문 행을 그룹화하는 태그

### 예제
> -	<head>안에 CSS코드를 입력하면 테두리가 나타난다.<br>
  
```html
<style>
    th, td { border: 1px solid; }
</style>
```

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8" />
    <title>내가 좋아하는 만화</title>
    <style media="screen">
      td,
      th {
        border: 1px solid;
      }
    </style>
  </head>
  <body>
    <table>
      <caption>
        좋아하는 만화 종류
      </caption>
      <thead>
        <tr>
          <th rowspan="2">웹툰</th>
          <th rowspan="2">만화</th>
          <th colspan="2">기타</th>
        </tr>

        <tr>
          <th>애니</th>
          <th>카툰</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>신의 탑</td>
          <td>원피스</td>
          <td>주술회전</td>
          <td>없음</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td>광장</td>
          <td>강철의 연금술사</td>
          <td>하이큐</td>
          <td>있음</td>
        </tr>
      </tfoot>
    </table>
  </body>
</html>
```

<table>
  <caption>
      좋아하는 만화 종류
  </caption>
  <thead>
   <tr>
    <th rowspan="2">웹툰</th>
    <th rowspan="2">만화</th>
    <th colspan="2">기타</th>
   </tr>

   <tr>
     <th>애니</th>
     <th>카툰</th>
   </tr>
  </thead>
   <tbody>
    <tr>
      <td>신의 탑</td>
      <td>원피스</td>
      <td>주술회전</td>
      <td>없음</td>
    </tr>
   </tbody>
   <tfoot>
    <tr>
      <td>광장</td>
      <td>강철의 연금술사</td>
      <td>하이큐</td>
      <td>있음</td>
    </tr>
  </tfoot>
</table><br>
  
[🚀위로 가기](#목차)
<br><br>

## 폼 요소
> 웹 사이트가 사용자로부터 데이터를 받아야하는 경우 사용되는 요소 ex)아이디,비밀번호 입력

```html
<input type="type 종류">
```
### input과 같이 사용되는 type 종류
1. `text 타입`: 주로 단순한 텍스트를 입력할 때 사용
   - `placeholder 속성`: 사용자가 입력하기전 미리 노출하는 값
2. `password 타입`: 암호와 같이 공개할 수 없는 내용을 입력할 때 사용
3. `radio 타입`: 라디오 버튼을 만들 때 사용 (중복선택 불가)
4. `checkbox 타입`: 체크박스를 만들 때 사용 (중복선택 가능)
   - 라디오 버튼과 체크박스에는 `checked`와 `name` 속성이 존재한다
      - `checked 속성`: 라디오버튼이나 체크박스의 체크 상태를 나타내는 속성. (defalut=False, 체크되지 않음)
      - `name 속성`: 그룹화 시키는 속성
5. `file 타입`: 파일을 서버에 올릴 때 사용
6. `submit 타입`: form의 값을 전송하는 버튼
7. `reset 타입`: form의 값을 초기화하는 버튼
8. `button 타입`: 아무 의미 없는 버튼
9. `image 타입`: 이미지를 삽입할 수 있는 버튼 


[🚀위로 가기](#목차)
<br><br>
