# Array 나 Object Deep copy 

## Array
```javascript
   var newArray = JSON.parse(JSON.stringify(oldArray)) 

   var newArray = oldArray.slice()
```

## Object
```javascript
    var newObject = Object.assign({}, oldObject);
```

단순 값만 복사한다면 위에 방법중 골라서 하면 된다.

다만 [{},{}]  나 {key:{},key:{}} 처럼

원소 값 또한 참조형이면 json 을 이용한 방식이 이외에는 결국에는 참조