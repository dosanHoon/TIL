# Vue data object 중 특정 키 값 삭제 하기
```javascript
delete Object.key
```
delete 로 data 삭제할경우 dom이 다시 render 되지 않았음.(진짜 거지같네...)

이럴때 Vue 에서 제공하는 API 사용해야 된다.

```javascript

Vue.delete( target, key )

// {Object | Array} target
// {string | number} key/index
// Only in 2.2.0+: Also works with Array + index.
```

React 에 비해서 자동으로 해주는 기능이나 제공되는 API 많은거 같아서 좋긴한데
순수 javascript에서 문제가 생기는 경우가 있는거 같은 느낌적인 느낌