# Trigger click on input=file on asynchronous ajax done()

- 파일 업로드 시 권한 체크할 필요가 있어서 서버 API Ajax 통신 후
  input file 을 click trigger 하려고 하면 되지 않는다.

  간단히 말하면 브라우저 보안 이슈 때문
  event 에 isTrust 라는 프로퍼티가 있어서 true 가 아니면 작동하지 않는 이슈

[참고](https://stackoverflow.com/questions/29728705/trigger-click-on-input-file-on-asynchronous-ajax-done)
[isTrust 참고](https://stackoverflow.com/questions/29728705/trigger-click-on-input-file-on-asynchronous-ajax-done)
