# Video-Trailer-Popup

<img src="./image.gif">

<br>

**버튼을 클릭을 하면 비디오 팝업이 나오도록 구현하였습니다.**

<br>

## 기능

비디오 플레이 기능을 구현

<br>

## 사용한 라이브러리
1.  fontawesome  
: https://fontawesome.com/

<br>

## 학습 
### 1. css : box-sizing
: 요소의 전체 너비와 높이에 패딩과 테두리를 포함할 수 있음  

: 기본적으로 요소의 너비와 높이는 다음과 같이 계산되는데, 
- 너비 + 패딩 + 테두리 = 요소의 실제 너비  
- 높이 + 패딩 + 테두리 = 요소의 실제 높이  

<br>

요소의 테두리와 패딩이 요소의 지정된 너비/높이에 추가되기 때문에 요소가 설정한 것보다 더 크게 나타나는 경우가 많음   

=> 이런 문제를 **box-sizing**으로 해결 할 수 있음
```
box-sizing: border-box;
```
요소에 설정하면 패딩과 테두리가 너비와 높이에 포함이 됨  
<br>

### 2. css : max-width를 사용하는 이유
: 주로 반응형 웹 디자인에서 화면에 따라 스타일을 적용할 때 자주 사용  
=> 데스크탑용의 가장 큰 화면 사이즈의 레이아웃을 기본으로, 점차 축소하는 형태로 css를 작성할 때 사용됨  
: 요소의 최대 너비를 정의  
: 콘텐츠가 최대 너비보다 크면 요소의 높이가 자동으로 변경  
: 내용이 최대 너비보다 작으면 max-width속성이 적용 안됨  
<br>

### 3. css : 요소를 중앙으로 정렬시키는 방법
**(1) 텍스트 중앙 정렬**    
```
text-align: center;
```
**(2) 블록 레벨 요소 중앙 정렬**  
```
 margin: 0 auto;
``` 
**(3) flexbox를 이용한 중앙정렬**  
```
display: flex;
justify-content: center;
align-items: center;
```

**(3) Transform과 Translate를 이용한 중앙정렬**  
```
.container {
  /* 부모 요소에 설정 */
  position: relative;
}

.child {
  <!-- 상하좌우 정중앙 정렬하기  -->
  <!-- 자녀의 position속성을 absolute -->
  position: absolute;
  top: 50%;
  left: 50%;
  <!-- 자식 요소 전체를 중앙 정렬하기 위해 -->
  transform: translate(-50%, -50%);
}

```
<br>

### 4. js : add, remove , toggle 
: classList 메서드
: add()는 클래스를 추가  
```
const list = element.classList;
list.add("myStyle");
```

: remove()는 클래스를 제거     
```
const list = element.classList;
list.remove("myStyle");
```
: toggle()은 add()와 remove()의 기능을 한번에 함 
```
const list = element.classList;
list.toggle("myStyle");
```


<br>

## 5. 학습출처  
**유튜브**   
https://www.youtube.com/@JavaScriptKing

**CSS**    
https://developer.mozilla.org/ko/docs/Web/API/HTMLMediaElement         
https://www.w3schools.com/  
https://despiteallthat.tistory.com/144  
https://www.freecodecamp.org/korean/news/cssro-mueosideun-jungang-jeongryeolhaneun-bangbeob-div-tegseuteu-deung   

**JS**     
https://www.w3schools.com/jsref/prop_element_classlist.asp  