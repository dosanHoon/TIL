#HTML TAG 동적으로 렌더링 하기

```javascript
import React from "react";

const DynamHTMLTag = ({ tag }) => {
  let Tag = tag;
  return <Tag />;
};
```

```javascript
<DynamHTMLTag tag="p" />
```
