 ```html
 <link rel="shortcut icon" href="%PUBLIC_URL%/favicon.ico">
 ```

 ```javascript
 render() {
  // Note: this is an escape hatch and should be used sparingly!
  // Normally we recommend using `import` for getting asset URLs
  // as described in “Adding Images and Fonts” above this section.
  return <img src={process.env.PUBLIC_URL + '/img/logo.png'} />;
}
 ```