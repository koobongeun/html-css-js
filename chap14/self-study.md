# 변수 알아보기
## 변수란
- 변수 : 프로그램을 실행하는 동안 값이 여러 번 달라질 수 있는 데이터
- 상수 : 값을 한번 지정하면 바뀌지 않는 데이터
  - ex) 나이 (변수) : 올해 연도 (변수) - 태어난 연도 (변수) + 1 (상수)
- 변수 선언의 규칙
  - 영어문자 + 언더스코어(_)+숫자로 구성
  - 예약어xxxx
  - 여러 단어를 연결할 변수 이름은 중간에 대문자
  - 의미 있는 변수 이름

## DO IT! 실습
  ```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>나이 계산하기</title>
</head>
<body>
    <script>
			var currentYear = 2021;
			var birthYear;
			var age;

			birthYear = prompt("태어난 연도를 입력하세요. (YYYY)", "");
      age = currentYear - birthYear + 1;
      document.write(currentYear + "년 현재<br>");
      document.write(birthYear + "년에 태어난 사람의 나이는 " + age + "세입니다.");
    </script>
</body>
</html> 
```

## 자료형 이해하기
- 자료형
  - 기본 유형 : 숫자형, 문자열, 논리형
  - 복합 유형 : 배열, 객체
  - 특수 유형 : undefined (자료형이 지정되지 않았을 떄의 상태, 변수 선언만 하고 값을 할당하지 않은 변수)
 
## 조건문 알아보기
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3의 배수 확인하기 1</title>
</head>
<body>
    <script>
        var userNumber = prompt("숫자를 입력하세요");

        if (userNumber % 3 == 0)
            alert("3의 배수입니다.")
        else
            alert("3의 배수가 아닙니다.")
    </script>
</body>
</html>
```
- 프롬프트 창에 숫자를 입력한 후 [확인] 버튼을 누르면 입력값이 3의 배수인지 알려주고, [취소]버튼을 누르면 입력이 취소
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3의 배수 확인하기 2</title>
</head>
<body>
    <script>
        var userNum = prompt("숫자를 입력하세요.");

        if(userNum != null){
            if(userNum % 3 == 0)
                alert("3의 배수입니다.")
            else
                alert("3의 배수가 아닙니다.")
        }
        else
            alert("입력이 취소 되었습니다.")
    </script>
</body>
</html>
```
- 중첩된 if~else 문 대신에 조건 연산자를 사용한다면
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>조건 연산자를 사용해 3의 배수 확인하기</title>
</head>
<body>
    <script>
        var userNum = prompt("숫자를 입력하세요");

        if(userNum != null)
        (userNum % 3 == 0)?alert("3의 배수 입니다.") : alert("3의 배수가 아닙니다.");
        else
            alert("입력이 취소되었습니다.");
    </script>
</body>
</html>
```

### 논리 연산자로 조건 체크하기
- OR 연산자는 피연산자 2개 중에서 true가 하나라도 있으면 true
- OR 연산자
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>조건문</title>
</head>
<body>
  <script>
    var numberOne = prompt("50미만의 숫자를 입력하세요.");
    var numberTwo = prompt("50미만의 숫자를 입력하세요.");

    if (numberOne < 10 || numberTwo < 10) 
      alert("두 개의 숫자 중 최소한 하나는 10 미만이군요.");
    else 
      alert("두 개의 숫자 중 10 미만인 수는 없습니다.");
  </script>
</body>
</html>
```
- and 연산자
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>조건문</title>
</head>
<body>
    <script>
      var numberOne = prompt("50미만의 숫자를 입력하세요.");
      var numberTwo = prompt("50미만의 숫자를 입력하세요.");

      if (numberOne < 50 && numberTwo < 50) 
        alert("두 개의 숫자 모두 50 미만이군요.");
      else 
        alert("조건에 맞지 않는 숫자가 있습니다.")
    </script>
</body>
</html>
```
## DO IT 실습 자리 배치도 만들기 1
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>자리 배치도</title>
</head>
<body>
  <h1>자리 배치도</h1>
  <script>
    var memNum = prompt("입장객은 몇 명인가요?");
    var colNum = prompt("한 줄에 몇 명씩 앉습니까?");

    if (memNum % colNum === 0) 
      rowNum = parseInt(memNum / colNum);
    else
      rowNum = parseInt(memNum / colNum) + 1;

    document.write("모두 " + rowNum + "개의 줄이 필요합니다.");
  </script>
</body>
</html>
```
## 반복문 알아보기
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>1에서 5까지 더하기</title>
	<style>
		body {
			font-size:1.5em;
			line-height:2;
			text-align:center;
		}
	</style>
</head>
<body>
	<script>
		var sum = 0;

		sum += 1;
		sum += 2;
		sum += 3;
		sum += 4;
		sum += 5;
		document.write("1부터 5까지 더하면 " + sum);
	</script>
</body>
</html>
```

### for문 사용하기
- for문은 초깃값 -> 조건 -> 명령 -> 증가식
### 중첩 for문 
- 안쪽 for문을 모두 실행 후 밖 for 실행
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>구구단 - for문</title>
</head>
<body>
	<h1>구구단</h1>
	<script>
		var i, j;
		
		for (i = 1; i <= 9; i++) {
			document.write("<h3>" + i + "단</h3>");
			for (j = 1; j <= 9; j++) {
				document.write(i +" X " + j + " = " + i*j + "<br>");
			}
		}
	</script>
</body>
</html>
```
### 구구단 스타일 시트 만들기
```
div {
  display:inline-block;
  padding:0 20px 30px 20px;
  margin:15px;
  border:1px solid #ccc;
  line-height:2;
}
div h3 {
  text-align:center;
  font-weight:bold;
}
```
### while문과 do~while문 사용하기
-while문으로 팩토리얼 만들기
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>팩토리얼 계산하기</title>
	<style>
		body {
			padding-top:20px;
			text-align:center;
		}
	</style>
</head>
<body>
	<h1>while문을 사용한 팩토리얼 계산</h1>

	<script>
			var n = prompt("숫자를 입력하세요.","10");
			var msg = "";

			if (n !== null) {
				var nFact = 1;
				var i = 1;
				
				while(i <= n) {
					nFact *= i;
					i++;
				}
				msg = n + "! = " + nFact;
			}
			else
				msg = "값을 입력하지 않았습니다.";

			document.write(msg);
	</script>
</body>
</html>
```
## 어떤 반복문을 사용해야 할까?
- for문은 초깃값과 반복 크기가 일정할 경우 ex) 차례대로 반복하는 문제
- while, do~while 문은 초깃값이나 반복 크기 없이 조건만 주어졌을 때 많이 사용 --> 어떤 조건을 만족하는 동안 반복 (조건 체크!!!)

## doit!
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>자리 배치도</title>
  <style>
    table, td {
      border:1px solid #ccc;
      border-collapse: collapse;
    }
    td {
      padding:5px;
      font-size:0.9em;
    }
  </style>
</head>
<body>
  <h1>자리 배치도</h1>
  <script>
    var i, j;
    var memNum = prompt("입장객은 몇 명인가요?");
    var colNum = prompt("한 줄에 몇 명씩 앉습니까?");

    if (memNum % colNum == 0) 
      rowNum = parseInt(memNum / colNum);
    else
      rowNum = parseInt(memNum / colNum) + 1;

    // document.write("모두 " + rowNum + "개의 줄이 필요합니다.");

    document.write("<table>");
    for (i = 0; i < rowNum; i++) {
      document.write("<tr>");
      for (j = 1; j <= colNum; j++) {
        seatNo = i * colNum + j;
        if (seatNo > memNum) break;
        document.write("<td> 좌석 " + seatNo + " </td>"); 
      }
      document.write("</tr>");
    }
    document.write("</table>");
  </script>
</body>
</html>
```
