# extends

```javascript
class ExampleComponent extends React.Component {
  clickHandler() {
    console.log("Click fired!");
  }
}

class RenderComponent extends ExampleComponent {
  render() {
    return (
      <div>
        <button onClick={this.clickHandler.bind(this)}>Click me!</button>
      </div>
    );
  }
}
```

[live sample](https://jsbin.com/julujeguci/1/edit?html,js,console,output)
