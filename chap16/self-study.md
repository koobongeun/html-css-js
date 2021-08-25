# 자바스크립트와 객체
## 객체 알아보기
- 객체 : 프로그래밍에서 객체는 여러 가지 의미로 해석할 수 있지만, 자바스크립트에서 객체는 프로그램에서 인식할 수 있는 모든 대상을 가리킨다는 정도로 이해한다.
- DOM : 웹 문서 자체도 객체이고 그 안에 삽입되어 있는 이미지와 링크, 텍스트 필드등도 모두 객체, 일반적으로 웹 문서에 삽입하는 요소는 document, image, link 객체 등이 있다.
- 브라우저 관련 객체 : 사용하는 브라우저 정보를 담고 있는 navigator 객체를 비롯해 history, location, screen 객체 등이 있다.
- 내장 객체 : 웹 프로그래밍을 할 때 자주 사용하는 요소는 자바스크립트 안에 미리 객체로 정의되어 있는데, 이를 내장 객체라고 한다.
### js에서 객체는 참조형태 즉, 객체 자체가 아니라 인스턴스의 형태로 만들어서 사용 >> 객체라는 틀이라면 그 틀을 기본으로 해서 계속 같은 모양으로 찍어 내는 것이 인스턴스 그리고 그 인스턴스에 식별자를 붙여 사용한다.
### Date 객체의 인스턴스 만들기
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>What time is it?</title>
	<style>
		body {
			font-size:2em;
			text-align: center;
		}
	</style>
</head>
<body>
	<script>
		var now = new Date();
		document.write("현재 시각은 " + now) ;
	</script>
</body>
</html>
```
## 자바스크립트의 내장 객체
### splice : 배열에서 특정한 부분만 잘라 낸다.
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Array 객체의 메서드</title>
</head>
<body>
  <p>splice 메서드 사용하기</p>
	<script>
    // 인수가 1개일 경우
    var numbers = [1, 2, 3, 4, 5];
    var newNumbers = numbers.splice(2);
    document.write("반환된 배열 : " + newNumbers + "<br>" );
    document.write("변경된 배열 : " + numbers );
    document.write("<hr>");

    // 인수가 2개일 경우
    var study = ["html", "css", "web", "jquery"];
    var newStudy = study.splice(2,1);
    document.write("반환된 배열 : " + newStudy + "<br>");
    document.write("변경된 배열 : " + study);
    document.write("<hr>");

    // 인수가 3개 이상일 경우
    var newStudy2 = study.splice(2, 1, "js");
    document.write("반환된 배열 : " + newStudy2 + "<br>");
    document.write("변경된 배열 : " + study);
	</script>
</body>
</html>
```
### pop : 배열의 마지막 요소를 꺼내 그 값을 결과로 반환한다.
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>Array 객체의 메서드</title>
</head>
<body>
	<script>
		var nums = [1, 2, 3];
		var chars = ["a", "b", "c", "d"];

		var numsChars = nums.concat(chars);
		var charsNums = chars.concat(nums);
		document.write("nums에 chars 합치면 : ", numsChars, "<br> chars에 nums 합치면 : ", charsNums);
		document.write("<hr>");

		var string1 = nums.join();
		document.write("구분자 없이 : ", string1);
		document.write("<br>");
		var string2 = chars.join('/');
		document.write("/ 구분자 지정 : ", string2);
		document.write("<hr>");

		var ret1 = nums.push(4, 5);  // 배열 끝에 추가
		document.write("length : ", ret1, " | 배열 : ", nums);  		
		document.write("<br>");
		var ret2 = nums.unshift(0);  // 배열 앞에 추가
		document.write("length : ", ret2, " | 배열 : ", nums);
		document.write("<hr>");

		var popped1 = chars.pop(); // 마지막 요소 꺼냄
		document.write("꺼낸 요소 : ", popped1, " | 배열 : ", chars); 
		document.write("<br>");
		var popped2 = chars.shift(); // 첫번째 요소 꺼냄
		document.write("꺼낸 요소 : ", popped2, " | 배열 : ", chars);
		document.write("<hr>");
	</script>
</body>
</html>
```
## DO IT 실습!!
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>독서 챌린지</title>
  <style>
    #container{
      margin:50px auto;
      width:300px;
      height:300px;
      border-radius:50%;
      border:2px double #222;
      background-color:#d8f0fc;
      text-align: center;
    }
    h1 {
      margin-top:80px;
    }
    .accent {
      font-size:1.8em;
      font-weight:bold;
      color:red;
    }
  </style>
</head>
<body>
  <div id="container">
    <h1>책 읽기</h1>
    <p><span class="accent" id="result"></span>일 연속으로 <br> 책 읽기를 달성했군요.</p>
    <p>축하합니다!</p>
  </div>  

  <script>
    var now = new Date("2020-10-15");      
    var firstDay = new Date("2020-10-01");

    var toNow = now.getTime();         
    var toFirst = firstDay.getTime();  
    var passedTime = toNow - toFirst; 

    passedTime = Math.round(passedTime/(1000*60*60*24));

    document.querySelector('#result').innerText = passedTime;
  </script>
</body>
</html>
```
