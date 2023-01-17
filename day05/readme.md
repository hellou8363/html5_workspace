## Study Record
\
**오디오 관련 태그 및 속성**  
```<audio src="경로" controls loop autoplay preload>```
- controls: 오디오 제어판
- loop: 반복 재생
- autoplay: 렌더링 후 자동 재생(현재 지원 X)
- preload: (사용자가 버튼을 누르면 바로 재생할 수 있도록)미리 브라우저에 로딩  

```
<audio controls>
  <sources src="경로" type="audio/mpeg">
</audio>
```  
type: 오디오 형식(mp3, wav, ogg) => ogg는 Safari에서만 미지원  
audio/mpeg => mp3, MIME type

\
\
**비디오 관련 태그 및 속성**  
```
<video src="경로" controls autoplay>
<video controls autoplay poster="이미지파일">
  <source src="경로" type="video/mp4 codecs=avc1, mp4a>
</video>
```  
- poster: 영상이 재생되기 전에 보여지는 썸네일 이미지
- codecs: 브라우저 내 코덱으로 대부분 재생 가능하지만 예전 브라우저 환경을 사용하는 사용자를 위한 설정

\
\
**embed 태그 사용**  
```<embed src="경로" type="image/bmp">```  
\
\
**object 태그 사용**  
```<object data="경로" type="application/pdf"></object>```  
- 이미지, PDF, HTML 문서 삽입 가능
- web site 경로의 경우 브라우저에 표시되지 않음  

\
\
**form 태그 사용**  
```
<form name="form1" action="http://localhost:8080" method="post">
  <input type="text" name="name" size="10" placeholder="이름을 입력해주세요." required>
  <input type="submit" value="전송">
  <input type="reset" value="다시작성">
</form>
```
form태그가 하나의 양식으로 여러 개의 양식(form)을 작성할 경우  
name값을 Unique하게 작성해야 한다(backend에서 name값을 사용).
- action: 전송할 위치 지정, 위치값을 지정하지 않으면 자기자신에게 전송 / 받음
- method: form data를 어떤 방식으로 전송할지 지정  
  GET: 민감한 정보는 GET방식으로 보내지 않으며, 최대 455문자까지 가능
  POST: 글자제한 X  
    post / get 방식에 따른 결과(입력값 => name: hello, major: 1234)
  - method="post": body(payload): name=hello&major=1234
  - method="get": Request URL: GET /?name=hello&major=1234 HTTP/1.1
- type: 입력값의 형식
- placeholder: 사용자에게 입력해야 할 값을 알려주는 용도(희미한 글자로 보여줌)
- size: 지정한 숫자의 개수만큼 문자(영문자 기준)를 입력할 정도의 사이즈, 지정하지 않으면 기본 사이즈
- required: 필수입력, 입력하지 않으면 submit이 되지 않음
- submit: form에 작성된 데이터를 전송
- reset: input에 입력된 값 초기화
```
<form>
  <fieldset><!-- input 태그를 묶어줌 -->
    <legend>개인 정보 입력</legend>
      <P>이름: <input type="text" name="name"></P>
      <P>학교: <input type="text" name="school"></P>
      <input type="submit" value="제출">
      <input type="reset" value="다시작성">
  </fieldset>
</form>
```
- ```<fieldset>```: input 태그들을 묶어줌
- ```<legend>```: input그룹의 이름

