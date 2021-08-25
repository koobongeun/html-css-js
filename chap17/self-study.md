# 문서 객체 모델
## 문서 객체 모델 알아보기
- 문서 객체 모델의 정의 : 자바스크립트를 이용하여 웹 문서에 접근하고 제어할 수 있도록 객체를 사용해 웹 문서를 체계적으로 정리하는 방법
## DOM 트리
```
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>DOM Tree 알아보기</title>
</head>
<body>
  <h1>Do it!</h1>
  <img src="images/doit.jpg" alt="공부하는 이미지">
</body>
</html>
```
- 부모 자식
    - 이렇게 부모와 자식 구조로 표시하면 마치 나무 형태가 되므로 DOM 트리라고 한다.
    - DOM 트리에서 가지가 갈라져 나간 항목을 노드라고 한다.
    - DOM 트리의 시작 부분인 html 노드를 나무 뿌리에 해당한다 해서 루트 노드라고 한다.
## DOM 요소에 접근하고 속성 가져오기
### DOM에 접근하기
- id 선택자로 접근하는 getElementById() 메서드
    - 요소명.getElementById("id명")
- class값으로 접근하는 getElementByClassName()메서드
    - 요소명.getElementByClassName("class명")
- 태그이름으로 접근하는 getElementByTagName()메서드
    - 요소명.getElementByTagName("태그명")
- 다양한 방법으로 접근하는 querySelector(), querySelectorAll()메서드
    - 노드.querySelector(선택자)
    - 노드.querySelectorAll(선택자 또는 태그)
- 웹 요소의 내용을 수정하는 innerText, innerHTML 프로퍼티
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>innerText, innerHTML 프로퍼티</title>
</head>
<body>
	<button onclick="inntext()">innerText로 표시하기</button>
	<button onclick="innhtml()">innerHTML로 표시하기</button>
	<h1>현재 시각: </h1>
	<div id="current"></div>
	
	<script>
		var now = new Date();

		function inntext(){
			document.getElementById("current").innerText = now;
		}
		function innhtml() {
			document.getElementById("current").innerHTML = "<em>" + now + "</em>";
		}
	</script>
</body>
</html>
```
- 속성을 가져오거나 수정하는 getAttribute(), setAttribute() 메서드
    -getAttribute("속성명")
    -setAttribute("속성명", "값")
```
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>DOM</title>
	<link rel="stylesheet" href="css/product.css">
</head>
<body>
	<div id="container">
		<h1 id="heading">에디오피아 게뎁</h1>
		<div id="prod-pic">
			<img src="images/coffee-pink.jpg" alt="에디오피아 게뎁" id="cup" width="200" height="200" onclick="displaySrc()">
				<div id="small-pic"> 
					<img src="images/coffee-pink.jpg" class="small">
					<img src="images/coffee-blue.jpg" class="small">
					<img src="images/coffee-gray.jpg" class="small">
				</div>
		</div>			
		<div id="desc">
			<ul>
				<li>상품명 : 에디오피아 게뎁</li>
				<li class="bluetext">판매가 : 9,000원</li>
				<li>배송비 : 3,000원<br>(50,000원 이상 구매시 무료)</li>
				<li>적립금 : 180원(2%)</li>
				<li>로스팅 : 2019.06.17</li>
				<button>장바구니 담기</button>
			</ul>				
			<a href="#" id="view">상세 설명 보기</a>				
		</div>
			
		<div id="detail">									
			<hr>
			<h2>상품 상세 정보</h2>
			<ul>
				<li>원산지 : 에디오피아</li>
				<li>지 역 : 이르가체프 코체레</li>
				<li>농 장 : 게뎁</li>
				<li>고 도 : 1,950 ~ 2,000 m</li>
				<li>품 종 : 지역 토착종</li>
				<li>가공법 : 워시드</li>
			</ul>
			<h3>Information</h3>
			<p>2차 세계대전 이후 설립된 게뎁농장은 유기농 인증 농장으로 여성의 고용 창출과 지역사회 발전에 기여하며 3대째 이어져 내려오는 오랜 역사를 가진 농장입니다. 게뎁 농장은 SCAA 인증을 받은 커피 품질관리 실험실을 갖추고 있어 철처한 관리를 통해 스페셜티커피를 생산합니다.</p>
			<h3>Flavor Note</h3>
			<p>은은하고 다채로운 꽃향, 망고, 다크 체리, 달달함이 입안 가득.</p>
		</div>
	</div>

	<script>
		function displaySrc() {
			var cup = document.querySelector("#cup");
			alert("이미지 소스 : " + cup.getAttribute("src"));
		}	
	</script>
</body>
</html>
```
## DOM에서 노드 추가, 삭제하기
### 노드 리스트란
- DOM에서 새로운 노드를 만들어 추가하거나 삭제하려면 노드리스트를 사용해야한다.
- 새로운 노드 추가 과정
    - 모든 HTML 태그는 요소노드
    - HTML 태그에서 사용하는 텍스트 내용은 자식 노드인 텍스트
    - HTML 태그에 있는 속성은 자식 노드인 속성 노드
    - 주석은 주석 노드
- 이 원칙에 따라 어떠한 태그를 노드로 추가한다면 단순히 태그에 해당하는 요소 노드뿐만 아니라 텍스트 노드와 속성 노드도 추가
### 텍스트 노드를 사용하는 새로운 요소 추가하기
- 요소노드 만들기 
    -createElement()메서드
    -document.createElement(노드명)
- 텍스트 노드 만들기 
    -createTextNode()메서드
    -document.createTextNode(텍스트)
- 자식 노드 연결
    -부모노드.appendChild(자식노드)
 ```
 <!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>DOM</title>
  <style>
    #container{
      width:500px;
      margin:10px auto;
      padding:20px;
    }
    #info {
      margin-top:20px;
    }
  </style>
</head>
<body>
  <div id="container">    
    <h1>DOM을 공부합시다</h1>
    <a href="#" onclick="addP(); this.onclick='';">더 보기</a>    
    <div id="info"></div>
  </div>
  <script>
    function addP() {
      var newP = document.createElement("p");
      var txtNode = document.createTextNode("DOM은 Document Object Model의 줄임말입니다.");
      newP.appendChild(txtNode);
      document.getElementById("info").appendChild(newP);
    }
  </script>
</body>
</html>
 ```
 
 ## Do IT
 ```
 <!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Web Programming</title>
	<link rel="stylesheet" href="css/nodelist.css">
</head>
<body>
  <div id="container">
    <h1>Web Programming</h1>
    <p>공부할 주제를 기록해 보세요</p>
    <form action="">
      <input type="text" id="subject" autofocus>
      <button onclick="newRegister(); return false;">추가</button>
    </form>
    <hr>  
    <ul id="itemList"></ul>  
  </div>

  <script>
    function newRegister() {
      var newItem = document.createElement("li");
      var subject = document.querySelector("#subject");
      var newText = document.createTextNode(subject.value);
      newItem.appendChild(newText);

      var itemList = document.querySelector("#itemList");
      itemList.appendChild(newItem);
      
      subject.value="";
    }
  </script>
</body>
</html>
 ```
