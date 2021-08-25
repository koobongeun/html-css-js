# 함수와 이벤트
## 여러 동작을 묶은 덩어리, 함수
- 개발자가 가져다가 쓰는 것
- alert(), propomt() popup() 등 ...
### 함수를 사용하지 않고 두 수 더하기 --> 여러 번 실행해야 한다면...?
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>함수</title>
	<style>
		body {
			padding-top:20px;
			text-align:center;
		}
	</style>
</head>
<body>
	<script>
		var num1 = 2;
		var	num2 = 3;
		var sum = num1 + num2;
		alert("결과 값: " + sum);
	</script>	
</body>
</html>
```
### 함수를 사용해 두 수 더하기 ---> 함수 선언 위치는 프로그램 흐름에 영향을 주지 않는다.
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>함수</title>
</head>
<body>
	<script>		
		function addNumber() { 								
			var num1 = 2;
			var num2 = 3;
			var sum = num1 + num2;			
			alert("결과 값: " + sum);
		}
		addNumber();
	</script>	
</body>
</html>
```
## var를 사용한 변수의 특징
- 한 함수에서만 사용할 수 있는 변수 : 지역변수 또는 로컬변수
- 스크립트 소스 전체에서 사용할 수 있는 변수 : 전역변수 또는 글로벌변수 ---> 적용 범위를 제한하지 않고 쓸 수 있음, var예약어를 빼고 선언 해야함.
### var 예약어를 사용한 지역변수와 전역변수
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>var 예약어를 사용한 지역 변수와 전역 변수</title>
</head>
<body>
	<script>		
		function addNumber() { 								
			var sum = 10 + 20;
      multi = 10 * 20;
		}
    addNumber();
    console.log(multi);    
  </script>
</body>
</html>
```

### var와 호이스팅(끌어올린다,, 실제로는 그런 식으로 해석한다는 뜻)
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>변수 호이스팅</title>
</head>
<body>
  <script>		 
    var x = 10;

		function displayNumber() { 								
      console.log("x is " + x);
      console.log("y is " + y);      
      var y = 20;
		}
    displayNumber();
  </script>
</body>
</html>
```
- js 해석기는 함수 소스를 훑어보면서 var를 사용한 변수는 따로 기억! 즉, 변수를 실행하기 전이지만 '이런 변수도 있구나' 하고 기억해 두기 때문에 마치 선언한 것과 같은 효과가 있는것 (호이스팅)

## let와 const의 등장
- 되도록이면 var예약어는 사용하지 않을 것을 권장
- var와 let, const의 가장 큰 차이는 스코프의 범위 >> var는 함수영역(레벨)의 스코프를 가지지만 let와 const는 블록 영역의 스코프
- let 예약어로 선언한 변수는 변수를 선언한 블록에서만 유효하고 블록을 벗어나면 사용x 즉, sum은 함수 calcSum()의 블록안에서만 사용 또한 for문의 카운터 변수 i도 let예약어
### 블록 변수 선언하기
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Function - Variable</title>
</head>
<body>
  <script>
    function calcSum(n) {
      let sum = 0;
      for(let i = 1; i < n + 1; i++) {						
        sum += i;	
      }      
      console.log(sum);
    }    
    calcSum(10);    
  </script>
</body>
</html>
```
### 전역 변수 선언하기
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Function - Variable</title>
</head>
<body>
  <script>
    function calcSum(n) {
      sum = 0;
      for(let i = 1; i < n + 1; i++) {						
        sum += i;	
      }            
    }    
    calcSum(10);    
    console.log(sum);
  </script>
</body>
</html>
```
### let 예약어를 사용하여 선언한 변수는 값을 재할당할 수는 있지만 변수를 재선언할 수는 없다.
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Function - Variable</title>
</head>
<body>
  <script>
    function calcSum(n) {
      let sum = 0;
      for(let i = 1; i< n + 1; i++) {						
        sum += i;	
      }      
      let sum;
      console.log(sum);
    }    
    calcSum(10);    
  </script>
</body>
</html>
```

## do it! 실습
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>1부터 n까지 더하기</title>
</head>
<body>
	<script>
    function calcSum(n) {
      var sum = 0;
            
      for(let i = 1; i < n+1; i++) {						
        sum += i;	
      }
      document.write("1부터 " + n + "까지 더하면 " + sum);
    }    

    var userNumber = prompt("얼마까지 더할까요?");
    if (userNumber !== null) {
      calcSum(parseInt(userNumber));
    }
    // 아래 소스는 '취소' 버튼을 클릭했을 때 null이 아닌 NaN을 반환함. 
    // var userNumber = parseInt(prompt("얼마까지 더할까요?"));
    // if (userNumber != null) calcSum(userNumber);
	</script>
</body>
</html>
```
