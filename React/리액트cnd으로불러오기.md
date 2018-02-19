#React 와 ReactDom Cdn 으로 불러오기

* jsp 파일 내에서 데이터를 javascript react 파일내로 전달해야 되는데 웹팩으로 번들하게 되면 어려움이 있다.
(혹시 다른 방법이 있다면 알고 싶....)

아래의 js 라이브러리를 cdn으로 제공해주는 사이트의 링크를 이용하거나

[ReactDom](https://cdnjs.com/libraries/react-dom)  
[React](https://cdnjs.com/libraries/react)

npm 으로 프로젝트내에 react 와 reactdom를 설치 했다면 node_modules 폴더 안에 설치된 폴더를 찾아서  
umd 라는 폴더안에 있는 js 파일중 프로젝트에 맞는 js 파일을 복사해서 가져오면 된다.


웹팩에서 번들한 모듈을 글로벌 스코프로 사용하기 위해서는 옵션을 지정해 줘야 한다.

```javascript
output: {
    path: __dirname + '/src/main/webapp/react/',
    filename: 'bundle.js',
    library: 'myLibrary',
    libraryTarget: 'var'
},
```
위에 
```javascript
library: 'myLibrary',
libraryTarget: 'var'
```
가 그것이다.

뭔가 이렇게 무식해 보이는 방법 사용하는 이유는 위에 말한것처럼 jsp 의 데이터를 react 컴포넌트에 주입시키기 위해서인데

```jsp
<c:if test="${!onpro}">
    <li>
        <span class="f-11 p-0">
            <a href="" class="f-11">
                <span id="" class="f-11 p-t-0">1</span>
            </a>
        </span>
    </li>
    <li>
        <span class="f-11 p-0">
            <a href="" class="f-11">
                <span id="" class="f-11 p-t-0">1</span>
            </a>
        </span>
    </li>
</c:if>
```

예를 들어 위와 같은 코드가 jsp 에 있을때 react 로 변경하기 위해선 onpro라는 jsp 단의 변수를 전달해줘야 돼는데 
그 방법을 찾은게

* In JSP

```jsp
<script src="/js/react.development.js"></script>
<script src="/js/react-dom.production.min.js"></script>
<script src="/react/bundle.js"></script>
var rootElement = document.getElementById('');
ReactDOM.render(<Test onpro={"${!onpro}"} />,rootElement)
```

이런식으로 jsp 안에서 변수를 props 로 전달하고 ReactDOM.render 를 실행하는 방법이다.  
(물론 처음부터 서버사이드 렌더링을 한다면 해결될 문제이긴 하지만)  
처음에 이렇게 했을때는 리액트 서버사이드 렌더링 자바에서 하는 방법을 몰랐고 지금은 기존 방식에 익숙핸것도 있다.
어떤 방법이 베스트 인지는 고민해봐야 할거 같다.