# 웹 문서에 다양한 내용 입력하기


## 텍스트 입력하기

### &lt;br&gt; 태그와 &lt;p&gt;의 차이점
- &lt;br&gt; 태그를 두 번 사용하면 빈줄이 생기면서 텍스트 단락이 나뉘어짐 >> 실제로 단락 X
- 실제 단락 생성을 하기 위해서는 &lt;p&gt; 사용
### 인용할 때 쓰는 &lt;blockquote&gt;
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>레드향</title>
</head>
<body>
    <h1>레드향</h1>
    <p>껍질에 붉은 빛이 돌아 레드향이라 불린다.</p>
    <p>레드향은 한라봉과 귤을 교배한 것으로<br> 일반 귤보다 2배~3배 크고, 과육이 붉고 통통하다.</p>
    <blockquote>비타민 c와 비타민 p가 풍부해<br> 혈액순환, 감기예방 등에 좋은 것으로 알려져 있다.</blockquote> <!-- 인용할 때 쓰는 태그 -->
</body>
</html>
```
### 텍스트 굵게 표시 &lt;strong&gt;, &lt;b&gt;
- 중요 내용 : &lt;strong&gt;
- 단순 굵기 : &lt;b&gt;
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>텍스트 굵게 표시하기</title>
</head>
<body>
    <h1>레드향</h1>
    <p>껍질에 붉은 빛이 돌아 <b>레드향</b>이라 불린다.</p>
    <p>레드향은 한라봉과 귤을 교배한 것으로<br> 일반 귤보다 2배~3배 크고, 과육이 붉고 통통하다.</p>
    <p><strong>비타민 c와 비타민 p</strong>가 풍부해<br> 혈액순환, 감기예방 등에 좋은 것으로 알려져 있다.</p>
</body>
</html>
```
### 텍스트 관련 태그
- &lt;abbr&gt; : 줄임말을 표시하고 title 속성을 함께 사용할 수 있다.
- &lt;cite&gt; : 웹 문서나 포스트에서 참고 내용을 표시한다.
- &lt;ins&gt;  : 공동 작업 문서에서 새로운 내용을 삽입한다.

## DO IT 실습
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>탐라국 입춘굿</title>
</head>
<body>
    <div id = "container">
        <h1>탐라국 입춘굿</h1>
        <p>탐라국 입춘굿은 입춘을 맞아 풍년을 기원하는 행사로, 제주도의 문화 축제 중에서 유일하게 탐라 시대부터 이어져 왔다.</p>
        <p>제주도에서는 입춘을 새철이라 한다.<br> 신구간이 끝나 하늘의 1만 8,000 신이 지상으로 내려와 새해 일을 시작하는 때이다.</p>
        <p>자세히 보기</p>
        <h2>일정</h2>
        <h2>먹거리</h2>
    </div>
</body>
</html>
```

## 목록 만들기
### 순서 있는 목록을 만드는 &lt;ol&gt;, &lt;li&gt; 태그
- &lt;ol&gt; : order list
- &lt;li&gt; : list
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>레드향 샐러드 레시피</title>
</head>
<body>
    <h2>레드향 샐러드 레시피</h2>
    <p><b>재료: </b> 레드향1개, 아보카도 1개, 토마토 1개, 샐러드 채소 30g</p>
    <p><b>드레싱: </b>올리브유 1큰술, 레몬즙 2큰술, 꿀 1큰술, 소금약간</p>
    <ol>
        <li>샐러드 채소를 씻어 물기를 제거한 후 먹기 좋게 썰어서 준비합니다.</li>
        <li>레드향과 아보카도, 토마토도 먹기 좋은 크기로 썰어 둡니다.</li>
        <li>드레싱 재료를 믹서에 한꺼번에 넣고 갈아줍니다.</li>
        <li>볼에 샐러드 채소와 레드향, 아보카도, 토마토를 넣고 드레싱을 뿌리면 끝!</li>
    </ol>
</body>
</html>
```
### 순서 없는 목록을 만드는 &lt;ul&gt;, &lt;li&gt; 태그
- &lt;ul&gt; : unordered list
- &lt;li&gt; : list
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>순서 없는 목록 사용하기</title>
</head>
<body>
    <h2>레드향 샐러드 레시피</h2>
    <p><b>재료: </b> 레드향1개, 아보카도 1개, 토마토 1개, 샐러드 채소 30g</p>
    <p><b>드레싱: </b>올리브유 1큰술, 레몬즙 2큰술, 꿀 1큰술, 소금약간</p>
    <ul>
        <li>샐러드 채소를 씻어 물기를 제거한 후 먹기 좋게 썰어서 준비합니다.</li>
        <li>레드향과 아보카도, 토마토도 먹기 좋은 크기로 썰어 둡니다.</li>
        <li>드레싱 재료를 믹서에 한꺼번에 넣고 갈아줍니다.</li>
        <li>볼에 샐러드 채소와 레드향, 아보카도, 토마토를 넣고 드레싱을 뿌리면 끝!</li>
    </ul>
</body>
</html>
```

## 표 만들기
### 표를 만드는 &lt;table&gt;, &lt;caption&gt; 태그
- &lt;table&gt; : 테이블
- &lt;caption&gt; : 테이블 제목

### 행을 만드는 &lt;tr&gt;태그와 셀을 만드는 &lt;td&gt;,&lt;th&gt; 태그
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>표 만들기</title>
</head>
<body>
    <h2>상품구성</h2>
    <table = border="1">
        <caption>선물용과 가정용 상품 구성</caption>
        <tr>
            <th>용도</th>
            <th>중량</th>
            <th>개수</th>
            <th>가격</th>
        </tr>
        <tr>
            <td>선물용</td>
            <td>3kg</td>
            <td>11~16과</td>
            <td>35,000원</td>
        </tr>
        <tr>
            <td>선물용</td>
            <td>5kg</td>
            <td>18~26과</td>
            <td>52,000원</td>
        </tr>
        <tr>
            <td>가정용</td>
            <td>3kg</td>
            <td>11~16과</td>
            <td>30,000원</td>
        </tr>   
    </table>
</body>
</html>
```

## 이미지 삽입하기
### 웹에서 사용하는 대표적인 이미지 파일 형식
- GIF : 표시할 수 있는 색상 수는 최대 256가지, 다른 이미지 파일 형식에 비해 파일 크기가 작아서 아이콘이나 불릿 등 작은 이미지에 주로 사용한다.
- JPG/JPEG : GIF보다 색상과 명암을 다양하게 표현할 수 있다. 이미지를 수정하고 저장하는 작업을 반복할 경우 화질이 떨어질 수도 있다.
- PNG : 네트워크용으로 개발된 파일 형식, 색상을 다양하게 표현하면서 투명한 배경도 만들 수 있어 웹에서 가장 많이 사용한다.
- % : 이미지 크기의 값을 퍼센트(%)로 지정하면 현재 웹 브라우저 창의 너비와 높이를 기준으로 이미지 크기를 결정
- px : 이미지 크기의 값을 픽셀(px)로 지정하면 이미지의 너비나 높이를 해당 픽셀 크기 만큼 표시
```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>이미지와 대체용 텍스트 삽입하기</title>
</head>
<body>
    <img src= "image/3x4.jpg" alt = "구본근"width="150">
    <h1>구본근</h1>
</body>
</html>
```

## 하이퍼링크 삽입하기
### 링크를 삽입하는 &lt;a&gt; 태그와 href 속성
- 기본형 : &lt;a href = "링크할 주소"&gt; 텍스트 또는 이미지 &lt;/&gt;
