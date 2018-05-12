#Path 설정

```javascript
app.set("views", path.join(__dirname, "../dist"));
```

```javascript
    app.set('views', __dirname + '../dist'))
```

* 이처럼 하면 string 으로 이어 붙이니 위가 맞는 방법
