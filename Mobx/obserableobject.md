# Observable Object

## 예제

```javascript
class selectedCheckStore {
@observable
  isAllCheckByPage = {}
}

@action
  handleAllCheck(page) {
      this.isAllCheckByPage[page] = false
  }
```

- 위와 같이 작성 하면 isAllCheckByPage 변화를 감지 하지 못함
- Mobx 4 이전 버젼에서는 obserable object 생성 당시에 가지고 있던 property 만 감지

  [MobX 4 and lower] When passing objects through observable, only the properties that exist at the time of making the object observable will be observable. Properties that are added to the object at a later time won't become observable, unless set or extendObservable is used.

```javascript
class selectedCheckStore {
@observable
  isAllCheckByPage = {}
}

@action
  handleAllCheck(page) {
    const newCheckByPage = {[page]:true, ...this.isAllCheckByPage}
    this.isAllCheckByPage=newCheckByPage
  }
```

- 위와 같이 object 자체를 대체하면 감지함
