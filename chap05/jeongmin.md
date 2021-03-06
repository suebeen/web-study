## 5장 : 프론트엔드 통합

### 라우팅

서버-사이드 라우팅

```java
일반적인 방식으로 페이지 이동시마다 서버에서 받아와 렌더링 하는 것이다.
```

클라이언트-사이드 라우팅

```
어떤 메뉴를 클릭했을 때 페이지를 이동하지 않고 업데이트되는데 이 때 url 역시 바뀝니다. 브라우저의 이전페이지, 다음페이지 버튼 역시 정상적으로 일반적인 웹페이지를 이동하듯이 적용됩니다.

이러한클라이언트 사이드 라우팅의 원리로는 HTML5 - History API의 pushState라는 메소드를 이용해 임의의 히스토리 기록을 만들어서 이동할 수 있습니다. 이 때 만들어진 히스토리의 페이지는 서버에서 제공하는 페이지가 아니기 때문에, 실제 페이지로 이동하는 것이 아니라 history api가 만들어낸 페이지로 이동하는 것입니다. 그렇기 때문에 http 요청을 보낼 수 있는 url은 아닙니다. 예를 들어 리액트 앱으로 빌드한 페이지를 새 창을 띄워서 들어가보면 get 요청을 보낼 수 없는 url이라고 뜹니다.
```

### 로그인 컴포넌트

```java
컴포넌트(Component)
컴포넌트는 개념적으로 props라는 input값을 받고나서, UI, 즉 View(state) 상태에 따른 
화면에 어떻게 출력이 되는지 Output을 React Element로 보여주는 함수를 뜻한다. 
그래서 합성을 통해 UI를 재사용할 수 있고, 독립적인 단위로 쪼개어 생각할 수 있게 한다.  
React API 공식문서에 따르면 상속을 따르는 대신 모듈로 따로 분리해 합성을 사용하길 권장한다.
```

### 로컬 스토리지를 이용한 액세스 토큰 관리

Session Storage 

- 브라우저를 닫으면 사라짐

Local Storage

- 브라우저를 닫아도 사라지지 않음

```java
localStorage.setItem("", "")
```
