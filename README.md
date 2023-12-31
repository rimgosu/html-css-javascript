### Hello Javascript!
![image](https://github.com/rimgosu/html-css-javascript/assets/120752098/c3f607f0-62fa-472f-b681-1ab9f73d2f3b)



### 유용한 단축키
- ctrl + k + f             : 코드 정렬

### 입출력
- document.write           : 웹페이지에 글쓰기
- console.log              : 글쓰기
- alert                    : 알림 출력

- prompt                   : 문자열로 반환하는 입력문
- confirm                  : 논리형 데이터로 반환 (확인/취소)

### 변수 선언
- 1. var                   : 선언 ; 재선언 O 재할당 O (과거 코드)
- 2. let                   : 변수 ; 재선언 X 재할당 O
- 3. const                 : 상수 ; 재선언 X 재할당 X
- number, string , boolean : 값을 넣을 때 자료형 결정, 기본 데이터 타입
- undefined, null          : 자바스크립트에서만 존재하는 자료형
- undefined                : 데이터, 자료형 모두 정의되지 않은 상태 (선언만 했을 경우)
- null                     : "데이터만" 정의되지 않은 상태 (값이 비어있는지 체크할때 사용)
- hoisting                 : var로 같은 변수 초기화해도 오류 안나는 이유
                            함수를 아래 쓰고 호출해도 동작이 되는 것도 호이스팅임. (함수 호이스팅)

### 연산자
- 1. 산술연산자             : +  -  *  %  [/]
- 2. 비교연산자             : == != >  >= <  <= [===] [!==]
- 3. 대입연산자             : =  += -= *= /= %=
- 4. 논리연산자             : && || !
- 5. 증감연산자             : ++ --
- 6. 삼항연산자             : 조건식 ? true일때 : false일때

- [    /      ]            : 나누기(실수 형태로 나옴)
- [    ==     ]            : 동등연산자
- [    ===    ]            : 일치연산자

### 배열
- let arr = []             : 배열 선언
- arr.length               : 배열 길이
- arr.push()               : append
- arr.pop()                : pop
- arr.splice()             : 삭제 splice(index, 삭제할 갯수)
- arr.indexOf()            : index
- arr.includes()           : 데이터 있는지 확인 (if a in arr:)
- arr.slice()              : 파이썬 슬라이싱
- ...items                 : 함수 내에서 여럿 매개변수로 받을 때, *args
- ``                       : 파이썬 """ """과 같은 기능
- `${var}`                 : f'{var}'

### Set
-  const _set = new Set()   : 셋 선언
-  _set.size                : 셋 길이
-  _set.add(value)          : 셋에 값 추가
-  let arr = [..._set]      : 셋 -> 리스트 

### Math
- Math.floor()             : 값 내림
- Math.random()            : 0~1사이 랜덤 값

### Date
- let date  = new Date();

- let year  = date.getFullYear();
- let month = date.getMonth()+1;
- let day   = date.getDate();

- let hour  = date.getHours();
- let min   = date.getMinutes();
- let sec   = date.getSeconds();

### 함수 선언 (표현식)
- 1. function intro() {}      : 함수 호이스팅 가능. (함수 호출 => 함수 생성 불가)
- 2. let intro2 = function {} : 익명함수 형태 (주소값 전달), 함수 호이스팅 불가능. (함수 호출 => 함수 생성 불가)
- 3. let intro3 = () => {}    : 화살표 함수, 함수 호이스팅 불가능.

### 객체(object)
> 여러 속성과 메소드를 하나의 변수로 묶음.
> key, value 구조 {key:value, key:value, key:value, ...}
- 1) 사용자 정의 객체
- 2) 브라우저 객체 (BOM & DOM; 브라우저에서 제공)
- BOM : browser object model  : 브라우저의 기능을 제어할 수 있는 객체를 제공
- DOM : document object model : HTML문서를 제어할 수 있는 객체를 제공
- 3) 내장 객체 (Array, Date, Math, ...; javascript에서 제공)

```
/* 사용자 정의 객체 */
    let person = {
        "name"        : "임명진",
        "age"         : 25,
        "gender"      : "남자",
        "favoritFood" : ["김치찌개", "제육볶음", "계란찜"],
        "intro"       : function () {
            console.log(`안녕하세요. 저는 ${this.name}입니다.`);
        }
    };
```
#### 접근 방법 
  - 1. person.name
  - 2. person["name"]
  - 3. person.intro()
- this     : "객체 내의 변수"를 의미.

#### DOM 
- const msg = document.getElementById("msg");
- msg           : &lt;h1 id="msg"&gt;날씨가 너무 흐리네요..&lt;/h1&gt;
- msg.innerText : "텍스트"       ; 날씨가 너무 흐리네요.. 
- msg.innerHTML : "html"        ; 날씨가 너무 흐리네요.. 

- msg.innerText : 값 변경        ; "비가 내릴 것 같네요.." 
- msg.innerHTML : html 문서 변경 ;"<a href='#'>비가 내릴 것 같네요..</a>"  

#### 버튼 객체에 이벤트 적용
- 1. btn.onclick = function(){console.log("함수실행!");}
- 2. btn.addEventListener("click", function() {console.log("함수2번째 실행!");});
- 2_1. 함수 따로 정의 후 적용: 
```
let getValue = () => {console.log("함수3번째실행");}
btn.addEventListener("click", getValue)
```

#### 객체 속성에 직접 접근
> 객체.속성
```
<input type="text" id="user-input">
const userInput = document.getElementById("user-input");
console.log(userInput.value);
```

#### 이벤트 & 이벤트 핸들러
- 1) 이벤트       : 웹 페이지에서 마우스, 키보드입력, 스크롤 등의 행위
- 2) 이벤트핸들러 : 이벤트가 감지되었을 때, 동작하는 함수

### jquery
> https://jquery.com/download/
- slim vs normal : silm에선 ajax, effect 없음.
- production vs development : 배포용(min) vs 개발용 / 공백 없음 vs 공백 있음
                            공백만큼 데이터 전송량이 많아져서 공백 없는 버젼도 배포한다.
- visual studio : 03.javascript - js - jquery-3.7.0.js
- eclipse       : Ajax - src - webapp - js - jquery-3.7.0.js 

#### jquery 문법
##### $(jQuery 객체) : 태그 선택자
- $("h1")          : document.getElementsByTagName("h1")
- $("#tit")        : document.getElementsById("tit")
- $("#tit").text() : document.getElementsById("tit").innerText
- $("#tit").html() : document.getElementsById("tit").innerHTML
    
- $("#tit").html("바꿀내용")          : html과 text에서 바꿀 내용 쓰기
- $("#tit").css({key:value,..})      : css 스타일 변경
```
$("#tit").css({backgroundColor:"green"})
* jQuery css 적용하는 key : "-" => "대문자" *
```
- $("#tit").on("click", function(){} : 이벤트 핸들러

### Ajax
#### ajax 구조
```
$.ajax({
        url : movieURL,
        success: function(res) {},
        error: function() {}
    });
```
##### ajax in eclipse (get 방식)
- webapp - 폴더 - ~.html일 경우 mapping:
- ../(매핑주소값)으로 매핑해줘야함. ex) url : "../ajax" 
> url:(매핑 주소 값),
data:{data:123,data2:"hi"},
또는 url:"(매핑 주소 값)?data=123&data2=hi"

##### function vs function() 
- 클릭했을 때 실행 vs 시작하자마자 실행

### json
> 다운로드    : https://mvnrepository.com/artifact/com.google.code.gson/gson/2.9.0 (jar 파일)
- 붙여넣기    : C:\Users\aischool\Desktop\study\web study\04_1 server\Ajax\src\main\webapp\WEB-INF\lib
- 한글로 보기 : response.setContentType("application/json; charset=UTF-8");
- 자세한 설명 : https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types

- JsonObject jsonobj = new JsonObject(); // json 객체 생성
- jsonobj.addProperty("data", "Hello");  // json 속성 추가

#### json Array
- json Array에 단순 값 추가 :
```
JsonArray jsonArr = new JsonArray();
jsonArr.add("json배열");
jsonArr.add("1234");
jsonArr.add("ture");
```

- json Array에 키-쌍 값 추가

```
JsonArray jsonArr2 = new JsonArray();
JsonObject jsonObj1 = new JsonObject();
JsonObject jsonObj2 = new JsonObject();
JsonObject jsonObj3 = new JsonObject();
```
    
```
jsonObj1.addProperty("메뉴명", "아메리카노");
jsonObj1.addProperty("가격", 2000);
jsonObj2.addProperty("메뉴명", "카페라떼");
jsonObj2.addProperty("가격", 2500);
jsonObj3.addProperty("메뉴명", "바닐라라떼");
jsonObj3.addProperty("가격", 2500);
```

```
jsonArr2.add(jsonObj1);
jsonArr2.add(jsonObj2);
jsonArr2.add(jsonObj3);
```

- coffeeDTO  :
- 1) name,price,size
- 2) 생성자
- 3) getter()
- 4) toString()

### javaToJson 
> java객체 -> JSON 데이터로 변환0)
```
ArrayList<coffeeDTO> list = new ArrayList<>();
list.add(new coffeeDTO("AMERICANO", 4500, "XL"));
list.add(new coffeeDTO("LATTE", 5000, "L"));
             
Gson gson = new Gson();
String jsonArr = gson.toJson(list);
```

