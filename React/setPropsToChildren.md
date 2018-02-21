# 전달받은 children 에 props 주입하기

* this.props.children 으로 받은 하위요소에게 props 로 데이터를 주고 싶을때 사용하는 방법

```javascript
1. React API를 이용해서 자식 요소에게 직접 주입 하는 방법

const Child = ({ doSomething, value }) => (
  <div onClick={() => doSomething(value)}>Click Me</div>
);

class Parent extends React.PureComponent {
  doSomething = value => {
    console.log("doSomething called by child with value:", value);
  };

  render() {
    const { children } = this.props;

    var childrenWithProps = React.Children.map(children, child =>
      React.cloneElement(child, { doSomething: this.doSomething })
    );

    return <div>{childrenWithProps}</div>;
  }
}

ReactDOM.render(
  <Parent>
    <Child value="1" />
    <Child value="2" />
  </Parent>,
  document.getElementById("container")
);
```

[참고](https://reactjs.org/docs/react-api.html#reactchildren)

2. context 를 사용하여 주입하는 방법

```javascript
class Child extends React.Component {
  render() {
    return (
      <div onClick={() => this.context.doSomething(this.props.value)}>
        Click Me
      </div>
    );
  }
};


// Access parent context by defining contextTypes
Child.contextTypes = {
  doSomething: React.PropTypes.func
};

class Parent extends React.Component {
  // passes the information down to its children
  getChildContext() {
    return { doSomething : this.doSomething };
  }

  doSomething(value) {
    console.log('doSomething called by child with value:', value);
  },

  render() {
    return <div>{this.props.children}</div>
  }
};

// make information available to its children
Parent.childContextTypes = {
  doSomething: React.PropTypes.func
};

ReactDOM.render(
  <Parent>
    <Child value="1" />
    <Child value="2" />
  </Parent>,
  document.getElementById('container')
);
```

* context 를 사용하면 모든 하위 노드에서 접근할수 있기 때문에 편해보이지만
prop를 통해 접근하는 방식보다 의존성이 높기 때문에 전역적인 데이터에만 사용하는것을 권장한다.