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
**form / input 태그 사용**  
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

\
\
**텍스트 공간 입력 양식**  
```
<textarea cols="30" rows="5">
  텍스트를 작성하는 공간입니다.
</textarea>
```  
textarea영역에 주석을 넣으면 그대로 출력되며 텍스트 공간은 사이즈 조절이 가능하다.  
- cols: 열 사이즈
- rows: 행 사이즈

\
\
**form - Radio Button**  
각 radio group은 name(전송파라미터값)이 같아야 하며, 값은 하나만 선택 가능하다.  
checked: 기본으로 선택되는 값  
```
<form>
  <h3>당신의 성별은 무엇입니까?</h3>
  <input type="radio" name="sex" value="male" checked />남자
  <input type="radio" name="sex" value="female" />여자
</form>
```   
\
\
**form - Check Box**  
여러 개의 값 선택 가능  
```
<form>
  <input type="checkbox" name="subject" value="HTML5">HTML5<br>
  <input type="checkbox" name="subject" value="CSS3">CSS3<br>
  <input type="checkbox" name="subject" value="JavaScript">JavaScript<br>
  <input type="checkbox" name="subject" value="Jquery">Jquery
</form>
```  
\
\
**Button 태그 사용**  
일반적인 button으로 사용하기 위해서는 type을 button으로 지정해줘야 한다.  
(지정하지 않으면 submit과 동일, form태그에 있는 모든 값이 backend로 전송됨).  
실무에서는 이미지 버튼을 많이 사용하며, name속성이 없으면 value속성값이 있어도 전송되지 않는다.  
```<button type="button"><img src="./img/html.bmp"></button>```
\
\
**Select Box**  
```
<select name="subject" multiple>
  <option value="1" selected>HTML5</option>
  <option value="2">CSS3</option>
  <option value="3">JavaScript</option>
  <option value="4">Jquery</option>
</select>
```  
값 선택을 하나만 할 수 있으며, size를 지정하면 지정한 만큼만 보이고  
나머지는 위, 아래로 이동하면서 볼 수 있다.  
value: 실제 전송되는 값  
multiple: 여러 개의 속성을 선택할 수 있음  
selected: 기본 항목 선택 지정  