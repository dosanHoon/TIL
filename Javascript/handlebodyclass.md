#body tag class 변경하기

* react component 안에서 body tag class 를 변경할일이 있어서 찾다가 못보던 property 발견

```javascript
import React from 'react'

class BodyColor extends React.Component {
  static propTypes = {
    isDark: React.PropTypes.bool
  }
  static defaultProps = {
    isDark: false
  }
  componentDidMount() {
    document.body.classList.toggle('darkClass', this.props.isDark)
  }
  componentWillReceiveProps(nextProps) {
    document.body.classList.toggle('darkClass', nextProps.isDark)
  }
  componentWillUnmount() {
    document.body.classList.remove('darkClass')
  }
  render() {
    return this.props.children
  }
}
```

```javascript
    document.body.classList.toggle('{class 이름}', {참,거짓 값})
  
    document.body.classList
  
    document.body.classList.remove('{class 이름}')
```
