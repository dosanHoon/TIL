# import 절대경로로 하기

.env 파일 생성

```
NODE_PATH = src/
```

내용 추가

## vscode 설정

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "moduleResolution": "classic",
    "paths": {
      "*": ["*", "src/*"]
    }
  }
}
```
