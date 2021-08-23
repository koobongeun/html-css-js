# HTML과 첫 만남
## HTML이란 
1. 웹 문서를 만드는 언어
2. HyperText Markup Language
## HTML 구조 파악하기
```
<!DOCTYPE html>   <!-- 현재 문서가 HTML5 언어로 작성한 웹 문서라는 뜻 -->
<html lang = "ko">    <!-- 웹 문서의 시작과 끝을 나타내는 태그 -->
    <head>    <!-- 웹 브라우저가 웹 문서를 해석하는 데 필요한 정보를 입력하는 부분 -->
      <meta charset="UTF-8">
      <title> HTML 기본 문서</title>
      <style>
        h1 {padding : 10px;
        background-color : #222;
        color: #fff;
        }
      </style>
    </head>
    <body>    <!-- 실제로 웹 브라우저 화면에 나타나는 내용 -->
        <h1> 프론트엔드 웹 개발</h1>
        <hr>
        <p>HTML</p>
        <p>CSS</p>
        <p>자바스크립트</p>
    </body>
</html>
```
### &lt;meta&gt; 태그
- 데이터에 관한 데이터
    - 웹 문서와 관련된 정보를 지정
    - 어떤 인코딩을 사용할지 지정 ex) utf-8

## HTML 파일 만들기
### Do it! 실습
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <title>첫 번째 웹 문서 연습</title>
    <link rel ="stylesheet" href="style.css">
</head>
<body>
    <h1>웹 문서 만들기</h1>
</body>
</html>
```

## 웹 문서 구조를 만드는 시맨틱 태그
- 시맨틱(semantic) : 이름만 봐도 의미를 알 수 있다. ex) &lt;p&gt;, &lt;a&gt; 등..
- 시맨틱 태그를 사용하면 웹 브라우저가 HTML의 소스 코드만 보고도 어느 부분이 제목이고 메뉴이고 본문 내용인지 쉽게 알 수 있다.
- 문서 구조가 정확히 나눠지므로 PC나 모바일의 웹 브라우저와 여러 스마트 기기의 다양한 화면에서 웹 문서를 표현하기가 쉽다.
- 인터넷에서 웹 사이트를 검색할 때 필요한 내용을 정확히 찾을 수 있다.
### 웹 문서 구조를 만드는 주요 시맨틱 태그
1. 헤더 : 사이트 제목, 로고, 네비게이션, &lt;header&gt;, &lt;nav&gt;
2. 본문 : 본문 내용, &lt;section&gt;
3. 푸터 : 개발자 이름, 번호, 주소, sns, &lt;footer&gt;
