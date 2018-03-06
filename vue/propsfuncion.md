# function 에 parameter 전달 하기

```html
<button @click="swim(data)">
```

react 에서는 onClick 에 명시한 function 에 파라미터 넘겨 줄려면 .bind 사용 해야 했던거에 비하면
정말 직관적이다.
근데 문제가 props 의 function 과 컴포넌트의 function 이름이 같을 때 어떻게 해야 되지...