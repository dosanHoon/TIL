# React Router v4
## withRouter

* v3에서는 router 의 자식 컴포넌트는 자동으로 router 정보를 props 로 넘겨주었던거 같은데 v4
에서는 명시적으로 넘겨줘야 하나 보다

```java
  import {withRouter} from 'react-router-dom';
    ...

    const SomeComponent = withRouter(props => <MyComponent {...props}/>);

    class MyComponent extends React.Component {
        ...
        SomeMethod () {
          const {pathname} = this.props.location;
          ...
        }
        ...

    }
```

이런식으로 withRouter 컴포넌트로 한번 감싸줘야 router 의 state 나 context에 접근 할수 있다.
