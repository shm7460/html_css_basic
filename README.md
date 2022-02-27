# html

```html
<!DOCTYPE html>
<html>
    <head>
        <body>
        </body>
    </head>
</html>
```

1. 브라우저 화면상에 보여질 내용은 모두 body  태그에 있어야됨 head태그는 보여지지가 않음

2. 동시에 텍스트를 변경하려면 태그에 마우스를 클릭한 후 ctrl+d 클릭하면됨

   연속으로 ctrl+d 누르면 여러개 선택가능함

2. alt 누르고 클릭하면 동시에 입력가능

4. 글자 맨끝에 가는방법: end 클릭
   키보드로 스크롤해서 복사하기 shift +방향키
   div*4 :태그 4개생김

   주석처리:ctrl+/
   
   메모장에 제목쓰기 : #띄워쓰기+제목
   
3. html tags mdn 이라고 검색하고 정리된거 보기https://developer.mozilla.org/ko/docs/Web/HTML/element

4. https://www.w3schools.com/

5. 폴더명,파일명은 무조건 소문자로 만들기

6. 설피파일 (VSC)

   commmunity material theme (배경색)

   Material Icon Theme (아이콘)

   Prettier(내용 바르게 수정해줌)설치-왼쪽하단에 톱니바퀴클릭-세팅클릭-editor검색-Format On Save 찾아서 박스체크하기

   

## body

1. 글자 굵기 (h6까지 있음)

```html
 <h1>hello</h1> 
```

2. unordered list 

```html
<ul>
    <li>beer</li>
    <li>beer</li>
</ul>
```

3. ordered list 

```html
<ol>
    <li>beer</li>
    <li>beer</li>
</ol>
```

4. list item

```html
<li>beer</li> 
```

5. a(anchor)안의 href가 Go to google.com 글자를 구글로 이동시켜준다 (오직 a태그만이 href를 추가할수있음)

```html
<a hredf="https://www.google.co.kr/"> Go to google.com

</a>
```

6. target="blank" 는 글자를 클릭하면 <u>새창으로 열어서</u> 구글로 이동시켜줌

```html
<a hredf="https://www.google.co.kr/" target="_blank"> Go to google.com

</a>
```

7. 이미지태그는 셀프로 닫는 태그이다 (img태그만이 src 를 추가할수있다)

```html
<img src="이미지 주소"/>
<img src="img/img.png"/>
```

→ 같은폴더안에 이미지 사진이 있어야됨 img/img.png 는img라는 폴더안에 img.png이름의 사진이다라는 뜻

8. 태그문법 <tagname attribute name="attrvalue">content</tagname>

```html
<form>
      <input required placeholder="name" type="text" />
      <input required type="password" minlength="10" />
      <input required type="submit" value="ok" />
      <input type="file" accept="pdf" />
    </form>
```

9. id 는 고유값이어야한다 ,태그는 하나의 아이디만 가질수있다(id와 for의 값은 같아야됨)


```html
 <form>
      <label for="website">webits</label>
      <input id="website" required placeholder="name" type="email" />
      <input required type="submit" value="ok" />
    </form>
```

10시맨틱 태그(Sementic Tag) = div=  header,main,footer(박스기능)

```html
 <body>
    <header>
      <h1>the hyemin times</h1>
    </header>
    <main>hello</main>
    <footer>&copy: 2020 n.c</footer>
  </body>
```

11. 한줄로만 출력되게 해줌  span= address<-주소일때는 굳이 스팬쓸필요없음

```html
 <span>123 Road Altavista</span>
```



## head

1. mata태그는 부가적인 정보이고 셀프로닫는 태그이다

```html
<head>
       <mata name="description" content="This is my websit"/>
 </head>
```

2. 한글,특수문자언어등입력할때 깨지지않게 해줌

```html
 <meta charset="utf-8">
```

3. 검색엔진에 도움을주고 사이트에 사용되는 언어를 말해줌

```html
<html lang="kr"> </html>
```

4.  웹사이트의 주소록의 이미지설정하는 태그임

```html
 <link

    rel="shortcut icon"
    sizes="16x16 32x32 64x64"
    								      href="https://www.youtube.com/s/desktop/12d6b690/img/favicon.ico"

  />
```

5. 링크를 복사해서 모바일로 볼떄 보여지는 소스들

```html
<meta property="og: title" content="hye min"/>  
<mata name="description" content="This is my websit" />
<mata property="og:image" content="https://www.google.co.kr/"/>
```

6. 웹사이트 이름 설정하기


```html
<head>
    <title>home my first website</title>
</head>
```


# css

1. css를 HTML에 추가하는 2가지 방법

```html
<head>                                   
    <style>
        h1{
        color: yellowgreen;
        font-weight: 1000;
        text-decoration: underline;
        font-style: italic;
        font: size 50px;
        }
    </style>
</head> 
or
<head>
 <link href="
             +
             styles.css" rel="stylesheet" />
</head>
```

-css는 각죽이 세미콜론(;)으로 끝나야됨    -> 태그{속성이름:속성값;}

-속성이름은 띄어쓰기 하면안됨 공백은 - 이걸로채움

-css 코드순서는 결과에 영향을 준다 (적용되는건 마지막 코드가 적용됨)

2. block/inline

```
block요소들은 옆에 아무도 올수없다(대부분 요소가 block이다, div,p..)

inline은 옆에 다른요소가 올수있다,같은줄에 위치할수있음 (span,a,image,code..)

inline은 높이와 너비가 없다(내용이 있어야 모양이보임) - block는 높이와 너비가 있다
```

3. block/line속성 바꾸기 (div가 inline 속성이됨)

```html
<head>
    <style>
        div{display:inline;}
    </style>
</head>

```

inline은 높이와 너비를 가질수없다 그래서 내용을 입력해야 보인다

4. margin은 box의 border의 바깥에 있는 공간이다  

```html
<style>
    body 
    {   
        margin: top 10px;
        margin-left: 300px;
        background-color: thistle;}
</style>
```

```html
margin:0px; 4면다적용됨
margin:20px 15px;(상하 좌우)  
margin:20px 15px 50px 30px; 시계방향순서(위-오-아래-왼)
```

-body와 div 경계가 같다면  위아래margin은 똑같이 움직임 (collapsing margins현상)

서로 다른박스의 경계가 만나면 하나로 인식한다는 뜻

그래서 padding이라는 개념이 필요함!

5. Padding은 box의 경계로부터 안쪽에 있는 공간이다  (margin과 반대개념)

```html
<style>
 body {
        margin: 20px;
        padding: 20px;
        background-color: thistle;
      }
</style>
```

6. id 명을 통해 가르키는법 (#)          head-style-#....

```html
<head>
    <style>
      #first 
        {
        background-color: whitesmoke;
        width: 150px;
        height: 150px;
        }
    </style>
</head>

<body>
    <div id="first">
    </div>
</body>
```

7. border는 box의 경계이다  (* : 전체 적용한다는 뜻)  3.7

```html
<head>
    <style>
        *{
            border: 2px solid black;
        }
        dive{
            
            border: 2px soild black;
        }
    </style>
</head>
```

8. inline

```
inline은 높이와 너비가 없다

->margin : 좌우만 적용됨 / padding은 사방에 가질수있음

(margin을 위아래 주고싶으면 block으로 바꿔야됨)
```

9. id를 한군데로 모으기

```html
<style>
      body {
        margin: 20px;
      }
      span {
        background-color: teal;
      }
      #tomato,
      #tomato2,
      #tomato3
      {
          background-color: tomato;
      }
      }
    </style>
  </head>
  <body>
    <span>hello</span>
    <span id="tomato">hello</span>
    <span>hello</span>
    <span id="tomato2">hello</span>
    <span>hello</span>
    <span id="tomato3">hello</span>
    <span>hello</span>
  </body>
```

10. (.) 온점은 class 명이다

```html
 <head>
    <style>
      .tomato 
        {
        background-color: tomato;
        color: white;
        padding: 5px 10px;
        border-radius: 10px;
        }
    </style>
  </head>
  <body>
    <span>hello</span>
    <span class="tomato">hello</span>
    <span>hello</span>
    <span class="tomato">hello</span>
    <span>hello</span>
    <span class="tomato">hello</span>
    <span>hello</span>
  </body>
```

```html
#tomato : id="tomato"
.tomato : class="tomato"
```

11. class의 이름은 여러개 합치기 가능하다 (btn + teal+ tomato)

```html
   <style>
      body {
        margin: 20px;
      }
      .btn {
        padding: 5px 10px;
        border-radius: 10px;
      }

      .tomato {
        background-color: tomato;
        color: white;
      }
      .teal {
        background-color: teal;
      }
    </style>
  </head>
  <body>
    <span class="btn teal">hello</span>
    <span class="btn tomato">hello</span>
    <span class="btn teal">hello</span>
    <span class="btn tomato">hello</span>
    <span class="btn teal">hello</span>
    <span class="btn tomato">hello</span>
    <span class="btn teal">hello</span>
  </body>
```

12. inline-block (블럭을 보이는 인라인으로 바꿔줌) 잘사용은 안하는 방식임

```html
<style>
      body {
        margin: 20px;
      }
      div {
        display: inline-block;
        width: 50px;
        height: 50px;
        background-color: teal;
      }
    </style>
  </head>
  <body>
    <div></div>
    <div></div>
    <div></div>
  </body>
```

13.flex (내가 원하는곳에 박스를 둘수있게 해줌 유연하게 대처해줌)

```html
<head>
    <style>
      body {
        height: 100vh;
        margin: 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
      div {
        background-color: teal;
        width: 300px;
        height: 300px;
      }
    </style>
  </head>
  <body>
    <div></div>
    <div></div>
    <div></div>
  </body>
```

- 'display : flex' 는 자식에게 명시하지않고 부모에게 명시한다 (div의 부모는 body이다)

- justify-content(주축) / align-items(교차축)
  - 주축은 기본적으로 ''수평''이다 (row로 적용되어있음)
  - 교차축은 ''수직''이다
  
- 'height: 100vh;'는 교차축의 값을 적용시켜준다

  - 100vh라고 하면 body가 화면의 100%인것이다 

    100%영역안에서 교차축(수직)이 움직임(전체화면의 크기를 가짐)

  - height 를 주지않으면 기본값 영역이 작아서(body의 크기가 작아)

     움직여도 표시가 안남
  
  - vh는 화면크기에 따라 비율조정해줌

14. fl flex-direction: column 주축과 교차축의 설정이 반대로됨


```html
 flex-direction: column;
```

```html
 <style>
      body {
        height: 100vh;
        margin: 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-direction: column;
      }
      div {
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 20px;
        color: white;
        width: 300px;
        height: 300px;
        background-color: teal;
      }
      #second {
        background-color: yellow;
      }
    </style>
  </head>
  <body>
    <div>1</div>
    <div id="second">2</div>
    <div>3</div>
  </body>
```

- column은 주축은 수직이되고 교차축이 수평이됨(기본설정이 반대로됨)

- display: flex;  <-설정을 먼저 해줘야 나머지  밑에것들도 작동됨

  justify-content: center;

  ​    align-items: center;

   flex-direction: column;

15. flex-wrap

```html
flex-wrap: wrap;
```

wrap을 하게되면 명시된 사이즈로 반영이된다 

ex) 한줄에 들어가는 만큼 최대한 집어넣고 그게되지않으면 다음줄로 옮겨진다

16. position:fixed;  위치를 고정시켜줌

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      body {
        height: 1000vh;
        margin: 20px;
      }
      div {
        width: 300px;
        height: 300px;
        color: white;
        background-color: teal;
      }
      #different {
        top: 5px;
        left: 200px;
        position: fixed;
        background-color: wheat;
        width: 350px;
      }
    </style>
  </head>
  <body>
    <div></div>
    <div id="different"></div>
  </body>
</html>

```

top,left,right,bottom 하나라도 추가하면 맨앞에 레이어가 된다(margin, block을 신경안씀)

17. position: relative;

```html
 <style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      div {
        width: 300px;
        height: 300px;
        background-color: wheat;
      }
      .green {
        top: -10px;
        position: relative;
        background-color: teal;
        height: 100px;
        width: 100px;
      }
    </style>
  </head>
  <body>
    <div>
      <div class="green"></div>
    </div>
  </body>
```

position: relative 를 사용하면 top,right,left,bottom을 이용해서 요소의 처음 놓인 자리에서 상하좌우로 움직임

18. position: absolute;

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=, initial-scale=1.0" />
    <title>Document</title>
    <style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      div {
        width: 300px;
        height: 300px;
        background-color: wheat;
        position: relative;
      }
      .green {
        bottom: 0px;
        position: absolute;
        background-color: teal;
        height: 100px;
        width: 100px;
      }
    </style>
  </head>
  <body>
    <div>
      <div class="green"></div>
    </div>
  </body>
</html>

```

body가 기준이(부모가기준이됨) 되어 움직임 그러나 기준이되었으면 하는 곳에 

position: relative; 을 입력해주면 그곳이 기준이됨 부모가됨

19. pesudo selector (첫번째와 마지막째 div 색 바꾸기)

```html
<style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      div {
        width: 150px;
        height: 150px;
        background-color: wheat;
        position: relative;
      }
      div:first-child {
        background-color: tomato;
      }
      div:last-child {
        background-color: teal;
      }
    </style>
  </head>
  <body>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </body>
```

pesudo selector은 class나 id를 만드는 것 보다 훨씬 좋은 방법이다  div : first-child{      } 

- pesudo selector (두번째 네번째 span색바꾸기)  

```html
 <style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      span {
        background-color: tomato;
      }
      span:nth-child(2),
      span:nth-child(4) {
        background-color: teal;
      }
    </style>
  </head>
  <body>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
  </body>
```

span:nth-child( 숫자 ){      }

- pesudo selector (짝수로 span 색 바꾸기) 

```html
<style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      span {
        background-color: tomato;
      }
     span:nth-child(even){
         background-color: teal;
     }
    </style>
  </head>
  <body>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
  </body>
```

span:nth-child(even){      }

- pesudo selector (3번째마다 span 색 바뀌기)  

```html
<style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      span {
        background-color: tomato;
      }
      span:nth-child(3n + 1) {
        background-color: teal;
      }
    </style>
  </head>
  <body>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
    <span>hello</span>
  </body>
```

span:nth-child(3n + 1) {      }

20. Combinators  (부모안에있는 자식에게만 css적용하기)              

```html
<style>
p span{
        color: teal;
    }
</style>
 <body>
  <div>
      <span>hello</span>
      <p>
          ldkfgkldfkgflgkl kfsldfkdsl sfklgkslfkglfsgk
          <span>inside</span>
      </p>
  </div>
    </body>
```

p span{      }    p:부모 span:자식

-  Combinators  (부모 바로 밑에 자식에게만 적용하기)

```html
 <style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      span {
        background-color: yellowgreen;
        padding: 5px;
        border-radius: 10px;
      }
      div > span {
        text-decoration: underline;
      }
      p span {
        color: white;
      }
    </style>
  </head>
  <body>
    <div>
      <span>hello</span>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
        <span>inside</span>
      </p>
    </div>
  </body>
```

div > span{        } div:부모  span:자식

- Combinators  (다음으로 오는 요소에게 CSS 적용하기(형제찾기) )  

```html
<style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      span {
        background-color: yellowgreen;
        padding: 5px;
        border-radius: 10px;
      }

      p span {
        color: white;
      }
      p + span {
        text-decoration: underline;
      }
    </style>
  </head>
  <body>
    <div>
      <p>lkkkkkkkkkk</p>
      <span>hello</span>
    </div>
  </body>
```

p + span{     }   p다음으로 오는 형제 span에게 CSS적용

- Combinators  (p뒤 span이 바로뒤에 없어도 사용가능 )

```html
  <style>
      body {
        height: 1000vh;
        margin: 50px;
      }
      span {
        background-color: yellowgreen;
        padding: 5px;
        border-radius: 10px;
      }

      p span {
        color: white;
      }
      p ~ span {
        text-decoration: underline;
      }
    </style>
  </head>
  <body>
    <div>
      <p>lkkkkkkkkkk</p>
      <address>hi</address>
      <span>hello</span>
    </div>
  </body>
```

p ~ span{    } p바로뒤에 span 형제가 없어도 css적용가능

21. attribute  (name 포함한 모든 영역은 분홍색 적용)

```html
 <style>
      input {
        border: 1px solid wheat;
      }
      input:required {
        border-color: tomato;
      }
      input[placeholder~="name"] {
        background-color: pink;
      }
    </style>
  </head>
  <body>
    <div>
      <form action="">
        <input type="text" placeholder="First name" />
        <input type="text" placeholder="Last name" />
        <input type="password" required placeholder="password" />
      </form>
    </div>
  </body>
```

 input[placeholder~="name"]{       }          (~= "  "   ->    "   "을 포함한 모든것 )

22. States     (클릭하면 색바뀜)

```html
<style>
      button:active {
        background-color: tomato;
      }
    </style>
  </head>
  <body>
    <div>
      <button>Hello</button>
    </div>
  </body>
```

button:active {    }  

- States  (마우스를 위에 두면 색이 바뀜)      

```html
 <style>
      button:hover {
        background-color: tomato;
      }
    </style>
  </head>
  <body>
    <div>
      <button>Hello</button>
    </div>
  </body>
```

  button:hover {     }

- States (키보드로 선택하면 색이 바뀜) 

```html
 <style>
      input:focus {
        background-color: tomato;
      }
    </style>
  </head>
  <body>
    <div>
      <input type="text" />
      <input type="text" />
    </div>
  </body>
```

input:focus {        }

- States      (방문한 링크는 색이 바뀜)     

````html
<style>
      a:visited {
        color: tomato;
      }
    </style>
  </head>
  <body>
    <a href="https://www.youtube.com/">youtube</a>
  </body>
````

 a:visited {    }

- States    (자식의 상태에 따라 부모가 바뀐다)

```html
 <style>
      form {
        border: 1px solid salmon;
        display: flex;
        flex-direction: column;
        padding: 20px;
      }
      form:focus-within {
        background-color: tomato;
      }
    </style>
  </head>
  <body>
    <form action="">
      <input type="text" name="" id="" />
      <input type="text" name="" id="" />
      <input type="text" name="" id="" />
    </form>
  </body>
```

 form:focus-within 

 (form:부모  input:자식 / input중 하나가 focus가되면 form의 모습이 바뀐다)

- States (부모의 상태에 따라 자식이 바뀐다)

```html
 <style>
      form {
        border: 1px solid salmon;
        display: flex;
        flex-direction: column;
        padding: 20px;
      }
      form:hover input {
        background-color: tomato;
      }
   or
      form:hover input:focus {
        background-color: tomato;
      }
    </style>
  </head>
  <body>
    <form action="">
      <input type="text" name="" id="" />
      <input type="text" name="" id="" />
      <input type="text" name="" id="" />
    </form>
  </body>
```

 form:hover input {  }  (부모 form이 hover되면 자식 input의 상태가 바뀐다)

 form:hover input:focus {  } (부모form이 hover이되고 자식input이 focus가 되면 자식 

상태가 이바뀜)

23. Pseudo element    ::      (placeholder을 스타일해준다)

```html
<style>
      input::placeholder {
        color: tomato;
      }
    </style>
  </head>
  <body>
    <form action="">
      <input type="text" placeholder="name" />
    </form>
  </body>
```

input::placeholder {   }          (input에 있는 placeholder을 바꿔줌)


- Pseudo element    ::      (선택해서 드래그하면 스타일해준다)

```html
 <style>
      p::selection {
        background-color: yellowgreen;
        color: white;
      }
    </style>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque, adipisci
      esse fugit illum omnis quaerat tempore error est doloremque rerum vel
      blanditiis nobis animi optio. Vitae exercitationem animi molestiae culpa!
    </p>
  </body>
```

 p::selection {  }     (p를 드래그하면 스타일 해줌)

- Pseudo element    ::      (글자의 첫번째 글자만 스타일해줌)

```html
 <style>
      p::first-letter {
        font-size: 100px;
        background-color: yellowgreen;
        color: white;
      }
    </style>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque, adipisci
      esse fugit illum omnis quaerat tempore error est doloremque rerum vel
      blanditiis nobis animi optio. Vitae exercitationem animi molestiae culpa!
    </p>
  </body>
```

 p::first-letter {  }  

24. Color       (rgb)

```html
<style>
    p {
        background-color: rgb(252, 206, 0, 0.8);
    }
</style>
```

 #fff:흰색,#000:블랙  rgb(252, 206, 0, 0.8) 0.8은 투명도이다

25.  Custom property       (root)             

```html
<style>
      :root {
        --main-color: #fbbc05;
        --default-border: 1px solid var(--main-color);
      }
      body {
        height: 1000vh;
        margin: 50px;
      }
      p {
        background-color: var(--main-color);
      }
      a {
        color: var(--main-color);
        border: var(--default-border);
      }
    </style>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quia itaque
      reprehenderit ipsum maxime magnam aliquid fugiat, voluptatum velit, illum
      illo quas perferendis officiis unde doloribus consequuntur, dolores
      temporibus voluptas labore?
    </p>
    <div>
      <a href="#">website</a>
    </div>
  </body>
```

변수: --(dash2개)이름-(dash1개)이름   

 :root {
        --main-color: #fbbc05;
        --default-border: 1px solid var(--main-color);

----------------

 color: var(--main-color);
        border: var(--default-border);

# +css

1. transitions (어떤 상태에서 다른 상태로 가는 변화)  

```html
 <style>
      a {
        color: white;
        background-color: tomato;
        text-decoration: none;
        padding: 3px 6px;
        border-radius: 5px;
        font-size: 50px;
        transition: background-color 10s ease-in-out, 
            color 5s ease-in-out;
          
          or transition: all 5s ease-in-out; (<-변화하는 모든것을바꿀때)
      }
      a:hover {
        color: tomato;
        background-color: wheat;
        border-radius: 30px;
      }
    </style>
  </head>
  <body>
    <a href="#">Go home</a>
  </body>
```

-transitions이라는 속성은 state인 hover...가 없는 요소에 있어야된다 

-변화를 시키고 싶다면 state에도 변화할것을 적어야 transitions된다

-https://matthewlein.com/tools/ceaser 이사이트를 통해서 여러효과를 볼수있음

> 코드를 복붙 사용가능함 : transition: all 2s ->복사한거 cubic-bezier(0.95, 0.05, 0.795, 0.035);

2. transform

```html
transform: rotateY(35deg);
transform: translateX(-60px);
```

```html
 <style>
      img {
        border: 10px solid black;
        border-radius: 50%;
        transition: transform 5s ease-in-out;
      }
      img:hover {
        transform: rotatex(90deg) scale(0.5);
      }
    </style>
  </head>
  <body>
    <img src="img/img.png" alt="" />
  </body>
```

> https://developer.mozilla.org/ko/docs/Web/CSS/transform 이사이트에서 복붙가능

transition 기능이 transform의 기능을 비디오처럼 보이게해줌

3. keyframes  ( 애니메이션 만드는 규칙:  @keyframes 아무이름{ form{ }to{ } }   )

```html
 <style>
      @keyframes hyemin {
        from {
          transform: rotateX(0);
        }
        to {
          transform: rotateX(360deg);
        }
      }
      img {
        border: 10px solid black;
        border-radius: 50%;
        animation: hyemin 5s ease-in-out infinite;
      }
    </style>
  </head>
  <body>
    <img src="img/img.png" alt="" />
  </body>
```

자동적으로 애니메이션 실행 가능 (만든 애니메이션 실행시키기 위해서 입력하기

->   animation: hyemin 5s ease-in-out;)

4. %    (애니메이션 되돌아가는 것도 순서대로 돌리기)

```html
 <style>
      body {
        display: flex;
        height: 100vh;
        align-items: center;
        justify-content: center;
      }
      @keyframes hyemin {
        0% {
          transform: rotateX(0);
        }
        50% {
          transform: rotatey(180deg) translatey(100px);
          border-radius: 0%;
          border-color: chartreuse;
          opacity: 0;
        }
        100% {
          transform: rotateY(0);
        }
      }
      img {
        border: 10px solid black;
        border-radius: 50%;
        animation: hyemin 5s ease-in-out infinite;
        width: 500px;
      }
    </style>
  </head>
  <body>
    <img src="img/img.png" alt="" />
  </body>
```

> https://animista.net/play/basic/flip-2   transform효과 여러개있음

5. media Queries (스크린의 사이즈를 알수있음)

```html
 <style>
      body {
        display: flex;
        height: 100vh;
        align-items: center;
        justify-content: center;
        flex-direction: column;
      }
      div {
        background-color: teal;
        width: 200px;
        height: 200px;
      }
      @media screen and (max-width: 600px) {
        div {
          background-color: tomato;
        }
      }
      @media screen and (min-width: 601px) and (max-width: 800px) {
        div {
          background-color: wheat;
        }
      }
      @media screen and (min-width: 1200px) {
        div {
          background-color: turquoise;
        }
      }

      @media screen and (orientation: landscape) {
        div {
          background-color: black;
        }
      }
      @media screen and (orientation: portrait) {
        div {
          background-color: darkorchid;
        }
      }

      span {
        font-size: 36px;
      }
      @media screen and (orientation: landscape) {
        span {
          display: none;
        }
      }
    </style>
  </head>
  <body>
    <div></div>
    <span>please flip your phone</span>
  </body>
```

 @media screen and (max-width: 600px){ 요소 { css } }  => 너비가 600이하 까지만 적용함

media query는 and로 연결해서 쓰면됨=> 

@media screen **and** (min-width: 601px) **and** (max-width: 800px)

가로모드: (orientation: landscape) 세로모드:(orientation: portrait) 

 display: none; =>화면에 안보이게함

- 프린트 할때만 지정색 정할수있음

```html
@media print {
        body {
          background-color: tomato;
        }
      }
```

6.  레이아웃잡기

- **flex-direction**
  정렬할방향을 지정

  row/row-reverse/column/cplumn-reverse

- **justify-content**

​		flex요소들을 가로선 상에서 정렬

- **align-items**
  flex요소를 세로선 상에서 정렬한다
- **order**
   flex요소의 순서를 지정한다 
  ex) .red{order:-1;}
  기본값은 모두 0 이다.
- **align-self**
  지정된 align-items 값을 무시하고 flex 요소를 세로선 상에서 정렬한다
- **flex-wrap**
  flex요소들을 한줄또는 여러줄에 걸쳐 정렬한다
  nowrap: 모든 요소들을 한 줄에 정렬합니다.
  wrap: 요소들을 여러 줄에 걸쳐 정렬합니다.
  wrap-reverse: 요소들을 여러 줄에 걸쳐 반대로 정렬합니다.
- **flex-flow**
  flex-dirction 와 flex-warp 두개의 속성들을 합친것
  ex)flex-flow: column wrap; (띄어쓰기로 구분함)
- **align-content**
  세로선 상에 여분의 공간이 있는 경우 flex컨테이너 사이의 간격을 조절함

7. root

```html
:root {--이름지정: 값  ;}
```

태그(ex: <input>)에다가 CSS를 적용하고 싶을 때는 :  <-- 한개
태그가 가지고 있는 속성(ex: placeholder)에 CSS를 적용하고 싶을 때는 ::

8.  {} / []

- {}는 단순히  CSS를 선언할 때 사용
  []는 상위태그(ex: <form>)안에 여러개 하위태그(ex: <input>) 중에서 특정 속성(type="subit")을 가지고 있는 input태그에만 CSS를 적용하고 싶을때
   not([type="submit"])을 적용하게 되면 type이 "submit"이 아닌 애들만 적용되도록 함

# git

git: 파일의 변경내역을 계속해서 추적해주는(version control system)-수정내용을 알수있음

github는 파일내역과 파일들을 올려주는 *공간*

markdown 은 서식이 있는 문서작성할때 씀 (.md)   - markdown태그 공부해보기

1. git-scm.com 들어가서 다운로드하기

2. github.com 들어가서 계정을 만들고 로그인하기

3. github에서 새로운 repository 만드는 방법

( new클릭-Repository name에 공백없이 소문자로 폴더이름 작성-Descriiption에 폴더명에대한 설명작성-개인정보가없으면 Public로 지정하기(포토폴리오로 활용가능하기때문)-Create repsotpry 버튼클릭 )

4. github desktop 도구 사용해서 컴퓨터와  github사이트폴더 연결하기

( github desktop 들거가서 다운로드하기-sign in to github.com버튼 클릭-Authorize desktop 버튼클릭-비번입력-Open Github Desktop클릭-Continue클릭-yes~stats체크풀기-Finish버튼클릭-Clone a repository from the internet클릭-github에서 만든 폴더이름 검색-폴더명클릭하고 Clone 버튼클릭 )

5. github에 github desktop이용해서 작성한 코드 올리기

( 왼쪽 체크박스에 파일 체크하기-왼족 하단에 commit타이틀 적기-밑에 제목설명적어도됨-Commit to mater버튼클릭-상단에 Publish branch클릭)



