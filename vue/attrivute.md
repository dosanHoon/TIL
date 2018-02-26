# v-model
```html
<input type="text" v-model="toDoValue"/>
```

* 데이터를 핸들링 태그의 속성

# v-bind
```html
<a v-bind:href="property"/>

<a :href="property"/>
```

* HTML 속성에 대응 하는 속성

# props, v-for, key
```html
<Todo v-bind:todo="todo" v-for="(todo,index) in todoList" :key="index"/>
```

# click 이벤트
```html
<button v-on:click="handleEditable"/>

<button @click="handleEditable"/>
```

# props property
```javascript
export default {
  props : ['todo']
}
```
