# 자바스크립트와 첫 만남
## 자바스크립트로 무엇을 할까
- 웹의 요소를 움직이거나 포토 갤러리를 펼쳐 놓는 것처럼 웹 사이트 UI부분에 많이 활용
- 웹 애플리케이션을 만든다.
- 다양한 라이브러리를 사용할 수 있다.
- 서버 개발을 할 수 있다.

## 웹 브라우저가 자바스크립트를 만났을때
- 외부 스크립트 파일로 연결해서 자바스크립트 작성하기
```
var heading = document.querySelector('#heading');
heading.onclick = function(){
    heading.style.color = "black";
}
```
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>내부 자바스크립트 사용하기</title>
    <style>
        body{text-align: center;}
        #heading {color:blue;}
        #text{
            color: gray;
            font-size: 15px;
        }
    </style>
</head>
<body>
    <h1 id = "heading">자바스크립트</h1>
    <p id = "text">위 텍스트를 글릭해 보세요</p>

    <script src = "my_change-color.js"></script>
</body>
</html>
```

## 자바스크립트 용어와 기본 입출력 방법
-간단한 입출력 방법
- 알림 창 출력하기
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>알림 창 만들기</title>
</head>
<body>
    <script>alert("안녕하세요?");</script>
</body>
</html>
```
- 확인창 출력하기
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>확인 창 만들기</title>
</head>
<body>
    <script>
        var reply = confirm("정말 배경 이미지를 바꾸겠습니까?");
    </script>
</body>
</html>
```
- 프롬프트 창에서 입력받기
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>prompt</title>
</head>
<body>
    <script>
        var name = prompt("이름을 입력하세요.");
    </script>
</body>
</html>
```
- 웹 브라우저 화면에 출력을 담당하는 document.write() 문
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>document.write()문으로 제목 표시하기</title>
</head>
<body>
    <script>
        document.write("<h1>어서오세요</h1>");
    </script>
</body>
</html>
```
- 콘솔 창에 출력하는 console.log() 문
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>이름 받아서 콘솔 창에 표시하기</title>
</head>
<body>
    <h1>어서오세요</h1>
    <script>
        var name = prompt("이름을 입력하세요.");
        console.log(name+"님, 환영합니다.");
    </script>
</body>
</html>
```

## 자바스크립트 스타일 가이드
- 코딩 규칙이 왜 필요할까요?
  - 자바스크립트는 웹 문서에 동적인 효과를 주기 위해 출발한 언어이므로 다른 프로그래밍 언어에 비해 데이터 유형이 유연해서 곳곳에 사용자가 주의를 기울이지 않으면 오류가 발생
  - 오픈 소스에 기여하거나 누군가와 공유할 소스라면 코드를 더욱 깔끔하게 작성해야함
- 자바스크립트 소소를 작성할 때 지켜야 할 규칙
  - 코드를 보기 좋게 들여쓰기
  - 세미콜론으로 문장을 구분
  - 공백을 넣어 읽기 쉽게 작성
  - 소스코드를 잘 설명하는 주석을 작성
  - 식별자는 정해진 규칙을 지켜 작성
    - 식별자는 개발자가 자바스크립트의 변수, 함수, 속성 등을 구별하려고 이름 붙인 특정 단어를 의미
  - 예약어는 식별자 사용할수 없다.
