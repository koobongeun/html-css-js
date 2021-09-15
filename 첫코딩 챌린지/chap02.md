# 첫코딩 챌린지

## chap02 웹, HTML이 뭐지?

### 2.1 웹이 뭐지?

- 네트워크는 컴퓨터와 컴퓨터를 연결해주는 망.
- 이런 망들이 모여서 더 큰 네트워크인 인터넷이 됨.
- 네트워크와 인터넷은 통신 규약 기반으로 연결 (프로토콜) ex) tcp/ip

### 2.3 웹은 어떻게 동작하지?

- 인터넷은 클라이언트(요청)와 서버(응답) 사이를 오가며 동작



### 2.4 HTML은 또 뭐야?

- HTML (HyperText Markup Language)은 프로그래밍 언어가 아니다, 마크업, 즉 표시하는 언어
- 2.4.1 HTML 기본구조

```html
<!DOCTYPE html> <!--문서 유형에 대한 브라우저의 정보-->
<html>
    <head><!--페이지에 표시 x, 페이지 정보를 제공-->
        <meta charset="utf-8"> 
        <meta http-equiv="X-UA-Compatible" content="IE=edge"> <!--메타 데이터는 데이터를 설명하는 데이터 ( ex.작성자, 날짜 )-->
        <title>my first page</title> <!--html 문서 제목을 표현-->
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
    </head>
    <body>
        <p>Hello world!</p>
    </body>
</html>
```



### 2.5 나도 안다! 코딩 상식!

- 코딩 : 코드를 작성하는 일
- 프로그래밍 : 코드작성, 분석 및 구현, 디버깅, 컴파일, 테스트, 구현
- 코더보다 프로그래머가 되기까지 많은 노력과 시간이 필요
- 웹 페이지 : 하이퍼텍스트로 작성된 문서 (HTML)
- 웹 사이트 : URL 기반으로 인터넷에서 서비스되는 웹 페이지의 집합
- URL : Uniform Resource Locator은 네트워크에서 자원의 위치를 알려주는 규약

### 궁금증

- html 언어는 프로그래밍 언어가 아니고 마크업 언어 (CSS 포함)
- JavaScript도 프로그래밍 언어가 아닌가?
- 해결 : 미국 넷스케이프(Netscape)의 브렌든 아이크(Brendan Eich)가 개발한 **스크립트 프로그래밍 언어**