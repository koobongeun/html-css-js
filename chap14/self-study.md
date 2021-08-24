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
