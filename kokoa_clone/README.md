# Kokoa Clone 2020 Update

- 주석처리:  <!-- --> :ctrl+/

- 도큐먼트 단축키 : !

- 무료아이콘
  https://heroicons.dev/
  https://fontawesome.com/v5.15/icons?d=gallery&p=2&q=user (유료로 사용할거면 이메일주면됨,

- https://fontawesome.com/v5.15/how-to-use/on-the-web/styling/sizing-icons
  
  (아이콘의 사이즈를 볼수있음)

  무료로할거면 밑에 코드 복붙해서 body 마지막!에 넣기-무료아이콘 찾아서 코드 복사해서 html에 붙여넣기)

  ```html
   <script
        src="https://kit.fontawesome.com/6478f529f2.js "
        crossorigin="anonymous"
      ></script>
  ```

  ```html
  <i class="fas fa-battery-full fa-lg"></i>
  ```

  fa-lg  : 폰 사이즈 크게 하기

- 폰트

  https://fonts.google.com/ 

(폰트 선택- @import로선택해서 복사- css상단에 붙여넣어 추가하기-font-family복사해서 body{ 여기에 붙여넣기;} )

https://abcdqbbq.tistory.com/9 :reset css이다 브라우저의 스타일을 없앰

- 깃허브에 업로드 하기싫은 파일은 따로 빼는 방법

( VSC비주얼에서 .gitignore 라는 파일 만들기(무시하고 싶은 파일 이름을 기록하는 파일임)-

코드에 무시하고싶은 파일이름 적기(폴더면 /붙이고 적기) )

- styles.css 파일에는 모든 화면에 적용되는 css를 넣도록 하자 다른것들은 따로 

  @import하기 

## index

1. BEM(Block Element Modifier)규칙

```html
 <body>
    <div class="status-bar">
      <div class="status-bar__column"></div>
    </div>
  </body>
```

- class="status-bar__column"인 이유: class="status-bar"안에  column이라는 뜻으로써

​	쉽게 알수있게 하기위해 작성했음, 

- css작성할때 id인가 class 인가 헷갈리기 때문에 위에 방법으로 보통 html은 class로 모두 작성함

2. 버튼 코드작성하는 방법 2가지

```html
<body>
<input type="submit">
<button></button>
</body>
```

3. css를 html에 링크거는 방법  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="css/styles.css"/>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Welcome to Kokoa Clone</title>
  </head>
```

- <link rel="stylesheet" href="css/styles.css"/>

css폴더안에 있는 styles.css 파일을 html코드안에 링크를 건다.

4. class = .(dot)

```html
<div class="status-bar">
.
.
.
.status-bar{        }
```

5. reset css      (https://cssdeck.com/blog/scripts/eric-meyer-reset-css/)

(우리가 원하지않아도 브라우저가 알아서 html에 적용시키는 스타일을 없앨수있다

대부분의 태그에  margin:0, padding:0, border:0등을 가진 css파일이다)

```css
@import "reset.css";
```

@import -> styles.css에 reset.css 파일을 추가하기

6. 글자 두줄로 만들기

```css
.welcome-header__text {
  width: 50%;
}
```

7. flex-direction: column; 은 좌우로 말고 위아래로 놓여있게하기위해서(반대로)  

8. align-items: center; 은 교차축을 이용해 센터에 위치하게 만들어줌
9. not  (뭔가가 적용되는 걸 원하지 않을때)

```css
#longin-form input:not([type="submit"]) {
  border-bottom: 1px solid rgb(0, 0, 0, 0.2);
  transition: border-color 0.3s ease-in-out;
}
```

submit 아닐때만 밑에 코드를 적용시킨다라는 뜻

10. Cursor (포인터 모양을 다르게 해줌)

```css
 cursor: pointer;
```

11.  inherit (부모로 부터 색상을 상속받아 기본 링크의 블루색상을 부모의 색으로 바꿔줌)

```css
#longin-form a {
  text-align: center;
  text-decoration: none;
  color: inherit;
}
```

## Screen 2. 

1. form action="friends.html" method="get"

action: 어떤 페이지로 data를 보낼건지 지정

method: 2가지방식있음 POST(백엔드 서버에 정보를 전송)/ GET(보안에 취약함)

2. nav (navigation)

```html
<body>
<nav>
        <ul>
            <li>
                <a href=""></a>
            </li>
        </ul>
    </nav>
</body>
```

 보통 nav는 이런식으로 코드가 짜여져 있다

2-1.   VSC단축키(shortcut)            

```html
 <nav>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </nav>
```

 nav>ul>li*4>a     한문장만 쓰면 유효한 html을 만들어줌

3. 파일의 순서를 지키는게 정말 중요함

```css
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600&display=swap");
@import "reset.css";
@import "variables.css";
/* components */
@import "components/status-bar.css";
@import "components/nav-bar.css";
/* screens */
@import "screens/login.css";

body {
  font-family: "Open Sans", sans-serif;
}
```

첫줄에는 font를 import 하고 그다음에는 style를 reset하고 그리고 variables.css를 import하였다.(순서가 바뀌면 적용이 안됨 늦게 import의 우선순위가 바뀌기 때문)

4.  box-sizing: border-box;

```css
.nav {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #f9f9fa;
  padding: 20px 50px;
  box-sizing: border-box;
  border-top: 1px solid rgba(177, 177, 177, 0.2);
}
```

css에게 padding 20px 50px를 적용했지만 나의 box사이즈를 늘리지 말고 

그대로 둬라고 명령하는것 (padding값만큼 내box를 늘리지 말라고하는 것임)

5.  position: absolute; 를 쓰기위한 조건

```css
.nav__link {
  position: relative;
  color: #2f363e;
}

.nav__notification {
  background-color: tomato;
  width: 30px;
  height: 30px;
  border-radius: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-weight: 600;
  position: absolute;
  left: 15px;
  bottom: 15px;
}
```
nav__notification을 감싸고있는 nav_link(container)에게 position:relativ를 적용해준다

왜냐하면  body중심으로 움직인것을 가장가까운 부모기준으로 바꿔줘야 적용이되기때문

6. icon 은 text라고 생각하면됨  (아이콘의 색 바꿀때)

```css
#friends-display-link i{
    color: rgba(0, 0, 0, 0.3);
}
```

7. VSC 단축키  

```html
<div class="user-component__column"></div>
<div class="user-component__column"></div>
```

 .user-component__column*2 을 입력하면 바로 코드를 만들어줌

## Screen 3. 

1. 하나의 element에게 두개의 class를 가지는 경우

```html
<span class="nav__notification badge">1</span>
```

nav__notification 와 badge 이다

2. span 은 line 이라 margin이 적용이 안됨  (block로 적용해야됨)

```css
.recommended-friends span {
  margin: 110px 0;
  display: block;
  text-align: center;
}
```

3. 모든 글자를 대문자로 만든다 

```css
.open-post__hashtags {
  text-transform: uppercase;
}
```

4.  class 지정하는 또다른 방법   (open-post__members안에있는 divider 이다)

```css
.open-post__members .divider{    }
```

5.  position: absolute;

```css
.open-post__photo {
  position: relative;
}
.open-post__heart-count {
  background-color: rgba(0, 0, 0, 0.9);
  color: white;
  border-radius: 20px;
  padding: 5px;
  display: flex;
  align-items: center;
  position: absolute;
}
```

 position: absolute; 를  적용한 코드에서 relative father을 찾는다 

왜냐하면 absolute children은  relative father이 있어야 작동가능하기때문

그래서 father를 찾아서 position: relative;적어줘야됨 

6. z-index (layer 순서이다)

```css
#chat-screen .alt-header {
  top: 10px;
  z-index: 1;
}
```

 position: fixed;  이라서 적용가능했다 기본값은 0이다.

7.  flex-direction: column;

```css
.main-chat {
  margin-top: 150px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
```

이때 기준은 세로축이고  cross axis 는 수평이된다

 align-items: center; 중앙정렬을 하면 가운데로 옴

8. span 일때 margin주는법

```css
.message__author {
  opacity: 0.8;
  font-size: 15px;
  margin-bottom: 10px;
  display: block;
}
```

display를 block 을한다 

9.  order  (flex childer에게만 적용이된다)

```css
.message-row--own .message__time {
  order: 0;
}
.message-row--own .message__bubble {
  order: 1;
}
```

9-1  flex-direction (modifier기준으로 뒤집을수있다)

```css
.message-row--own .message__info {
  flex-direction: row-reverse;
}
```

10. justify-content (수평으로 작동)

```css
.message-row--own {
  display: flex;
  justify-content: flex-end;
}
```

11. forwards  (애니메이션의 마지막 값을 계속 가지고있게해줌 )

```css
@keyframes hidesplashscreen {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
    visibility: hidden;
  }
}
#splash-screen {
  background-color: var(--yellow);
  position: absolute;
  height: 100vh;
  width: 100vw;
  top: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 130px;
  animation: hidesplashscreen 1s ease-in-out forwards;
}
```

다시 처음상태로 돌아게하지않음 

보통이런 효과로 요소를 숨길때는css 만으로는 부족하기때문에 JavaScript를 사용해야한다 

11-1.  animation-delay: 

```css
  animation-delay: 1s;
```

애니메이션의 시작을 지연시켜준다

12. will-change

```css
.open-post__heart-count:hover i {
  will-change: transform;
  animation: heartbeat 1s linear infinite;
}
```

브라우저에게 어떤 것이 변할 것인지 말해주고 일종의 브라우저에게 렌더링 힌트를 주면서 도와주는 역할임 (이게 없으면 애니메이션 효과는 불안정하게 흔들림)

## branch

1. branch

실험적인 코드나 다른 버전의 코드들을 따로 저장하고 싶다면 brach하면된다 

두가지 버전의 코드가있지만 파일은 한개만 가지고있으면된다 

Git으로 클릭만으로 버전을 왔다갔다 할수있다 

main변경사항을 commit 무조건해주기 

2. Brach->Merge into Current Branch

brach 이름을 클릭하고 파란색 창을 클릭하면 brach소스를 main으로 복사할수있다

3. 

github에서 branch를 가지고 있으면 공짜로 Static호스팅을 할수있게 해줌(즉  누구나 자신의 웹사이트를 무료로 업로드 가능html/css/javascript만으로 이루어진 사이트이다 front-end만가능)

조건: pubic저장소여야함, branch이름은 gh-pages이여야함

4.github 수정해서 다시 올릴때

main 에서 수정을하고  commit 하기-> gh-pages branch클릭-> 위에Branch탭클릭->update from main 클릭->push클릭

