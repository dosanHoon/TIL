onClick 나 onChange 등 메소드에서 파라미터를 넘거야 되는 경우

```javascript
handleChange = name => value => {
  this[name] = value;
};

////중략
<InputText onChange={this.handleChange("이름")} />;
```
