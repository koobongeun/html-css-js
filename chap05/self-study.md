# 입력 양식 작성하기
## 폼 삽입하기
### 폼을 만드는 &lt;form&gt; 태그
- method
    - get : 데이터를 256~4,096byte까지 넘겨주기 가능, 주소 표시줄에 사용자가 입력한 내용이 그대로 드러나는 단점.
    - post : 입력한 내용의 길이에 제한받지 않고 사용자가 입력한 내용도 드러나지 않다.
- name : 자바스크립트로 폼을 제어할 때 사용할 폼의 이름을 지정
- action : <form>태그 안의 내용을 처리해 줄 서버 프로그램을 지정
- target : action 속성에서 지정한 스크립트 파일을 현재 창이 아닌 다른 위치에서 열도록 한다.
### 폼 요소를 그룹으로 묶는 &lt;fieldset&gt;, &lt;legend&gt; 태그
  - &lt;fieldset&gt; : 하나의 폼 안에서 여러 구역을 나누어 표시 ex) 개인 정보와 배송 정보
  - &lt;legend&gt; : &lt;fieldset&gt;를 묶은 그룹에 제목을 붙일 수 있다.
```
  <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>폼 요소를 그룹으로 묶어서 표현하기</title>
</head>
<body>
    <form action="" >
        <fieldset>
            <label>아이디(6자리 이상)<input type = "text"></label>
        </fieldset>
        
        <fieldset>
            <label for = "user-id"> 아이디 (6자리 이상) </label>
            <input type = "text" id = "user-id">
        </fieldset>
    </form>
</body>
</html>
```
### 폼 요소에 레이블을 붙이는 &lt;label&gt;태그
  - &lt;label&gt; : &lt;input&gt; 태그와 같은 폼 요소에 레이블을 붙일 때 사용
      - 레이블이란 입력란 가까이에 아이디나 비밀번호처럼 붙여 놓은 텍스트
  
## 사용자 입력을 위한 input 태그
```
  <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>간단한 로그인 폼 만들기</title>
</head>
<body>
    <form>
        <fieldset>
            <label>아이디 : <input type = "text" id = "userd_id' size = "10"></label> <!-- input type을 text로 하여 아이디 입력 창 구현 -->
            <label>비밀번호: <input type = "password" pw = "userd_pw size = "10"></label> <!-- input type을 password로 하여 비밀번호 입력 창 구현 -->
            <input type = "submit" value = "로그인">
        </fieldset>
    </form>
</body>
</html>
```
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>배송 정보 입력하는 폼 만들기</title>
</head>
<body>
    <ul>
        <li>
            <label for = "user_name">이름</label>
            <input type = "text" id = "user_name">
        </li>
        <li>
            <label for = "user_address"> 주소</label>
            <input type = "text" id = "user_address">
        </li>
        <li>
            <label for = "email">이메일</label>
            <input type = "email" id = "user_email"> <!-- input type을 email로 하여 email 입력 창 구현 -->
        </li>
        <li>
            <label for = "phone">연락처</label>
            <input type = "tell" id = "user_tell"> <!-- input type을 tell로 하여 전화번호 입력 창 구현 -->
        </li>
    </ul>
</body>
</html>
```
```
 <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>체크 박스와 라디오 버튼을 삽입하는 폼 만들기</title>
</head>
<body>
    <fieldset>
        <legend>상품 선택</legend>
        <P><b>주문할 상품을 선택해 주세요.</b></P>
        <label><input type = "checkbox" value="s_3">선물용 3kg</label>
        <label><input type = "checkbox" value ='s_5'>선물용 5kg</label>
        <label><input type = "checkbox" value = "f_3">가정용 3kg</label>
        <label><input type = "checkbox" value = "f_5"> 가정용 5kg</label>
        <p><b>포장 선택</b></p>
        <label><input type = "radio" name = "gift" value="yes">선물포장</label>
        <lable><input type = "radio" name = "gift" value = "no"> 선물포장 안함</lable>
        <p>제출</p>
        <lable><input type = "submit"></lable>
    </fieldset>
</body>
</html>
 ```
  
  ## DO IT!
  ### 회원 가입 신청서 만들기
  ```
  <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>회원가입 신청서 만들기</title>
</head>
<body>
    <div id = "container">
    <h1>회원 가입을 환엽합니다.</h1>
    <form>
    <fieldset>
        <legend>사용자 정보</legend>
    <ul>
        <li>
            <label for  ="uid">아이디</label>
            <input type = "text" id = "uid">
        </li>
        <li>
            <label for = "umail">이메일</label>
            <input type = "email" id = "umail">
        </li>
        <li>
            <label for = "upw">비밀번호</label>
            <input type = "password" id = "upw">
        </li>
        <li>
            <label for = "dpw">비밀번호 확인</label>
            <input type = "password" id = "dpw">
        </li>
    </ul>
    </fieldset>

    <fieldset>
        <legend>이벤트와 새로운 소식</legend>
        <label>
            <input type = "radio" name = "mailing"value="yes"> 메일 수신
        </label>
        <label>
            <input type = "radio" name = "mailing" value="no"> 메일 수신안함
        </label>
    </fieldset>
    <div id = button>
        <input type = "submit" value = "가입하기">
        <input type = "reset" value = "취소"> 
    </div>
</form>
</div>
</body>
</html>
  ```
  
  ## input 태그의 주요 속성
  ```
  <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>autofocus와 placeholder</title>
</head>
<body>
    <form>
        <fieldset>
            <legend>배송 정보</legend>
                <label for = "user-name">이름</label>
                <input type = "text" id = "user_name" autofocus> <!-- 자동으로 입력 커서 갖다 놓는 autofocus 속성 -->
                <br>
                <label for = "user-address">배송정보</label>
                <input type = "adress" id = "user_address">
                <br>
            <lable for = "phone">핸드폰 번호</lable>
            <input type = "tel" id = "user_tell" placeholder="- 빼고 입력해주세요." size = "20"> <!-- 힌트를 표시해 주는 placeholder 속성 -->
        </fieldset>
    </form>
</body>
</html>
  ```
  
  ```
  <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>readonly와 required</title>
</head>
<body>
    <div>
    <form>
        <fieldset>
            <legend>배송 정보</legend>
            <ul id = shipping>
                <li>
                    <label for = "prod">주문 상품</label>
                    <input type = "text" id = "prod" value = "상품용 3KG" readonly> <!-- 읽기 전용 필드를 만들어 주는 readonly 속성 -->
                </li>
                <li>
                    <label for = "user_name">이름</label>
                    <input type = "text" id = "user_name" autofocus required> <!-- 필수 입력 필드를 지정하는 required 속성 -->
                </li>
                <li>
                    <label for = "user_address">주소</label>
                    <input type = "text" id = "user_address" required>
                </li>
                <li>
                    <label for = "user_email">메일</label>
                    <input type = "email" id = "user_email" autofocus> <!-- 자동으로 입력 커서 갖다 놓는 autofocus 속성 -->
                </li>
                <li>
                    <label for = "user_tell">번호</label>
                    <input type = "tell" id = "user_tell" required> 
                </li>
                <li>
                    <label for = "date">날짜</label>
                    <input type = "datetime-local" id ="date">
                </li>
            </ul>
        </fieldset>
        <input type = "submit" value="주문하기">
        <input type = "reset" value = "취소하기">
    </form>
    </div>
</body>
</html>
  ```
 
## 폼에서 사용하는 여러가지 태그
  - &lt;textarea&gt; : 폼에서 텍스트를 여러 줄 입력하는 영역 ex) 회원가입 약관
  - &lt;select&gt;, &lt;option&gt; : 사용자가 내용을 직접 입력하지 않고 여러 옵션 중에서 선택하게 하려면 드롭다운 목록이나 데이터 목록 사용
  ```
  <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>드롭다운 목록 만들기</title>
</head>
<body>
    <div>
        <form>
            <fieldset>
                <label for = "prod1">
                    상품 선택
                </label>
                <select id = "pord1">
                    <option value="special_3" selected>선물용 3KG</option>
                    <option value="special_5">선물용 5KG</option>
                    <option value= "family_3">가정용 3KG</option>
                    <optgroup value= "family_5">가정용 5KG</optgroup>
                </select>
                <label for = "prod2">
                    포장 여부
                </label>
                    <input type = "text" id = "pord2" list = "pack" >
                    <datalist id = "pack">
                        <option value="package">포장</option>
                        <option value = "no_package">포장안함</option>
                    </datalist>
                    <br>

                <label>
                    <label for = "memo">메모</label>
                    <textarea cols = "40" rows="4" placeholder="남길 말씀이 있다면 여기에">
                    </textarea>
                </label>
            </fieldset>
        </form>
    </div>
    
</body>
</html>
  ```
