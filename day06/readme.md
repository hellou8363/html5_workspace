## Study Record
\
**input 태그의 타입**  
month, time, datetime-local, color, number, range, email, url, search, meter, progress  
\
\
**input 태그의 속성**
- autofocus: 렌더링 되자마자 포커스를 맞춘다.
- readonly: 읽기전용(수정 X)
- disabled: 비활성화(쓰기 X)
- autocomplete: 입력 창을 클릭하면 기존에 입력했던 값을 보여준다(자동완성).
- spellcheck: 맞춤법 검사 속성

\
\
**공간 분할 태그**  
- div: block요소, 다른 HTML 요소들을 하나로 묶어준다.
- span: inline요소, 텍스트의 특정 부분을 묶는데 사용한다.
        주로 텍스트의 특정 부분에 따로 스타일을 적용하기 위해 사용
- 각 태그가 block인지, inline인지 확인

\
\
**input type="file"**  
name 속성 필수, 다중 파일을 업로드 하기 위해서는 multiple 속성 추가  
\
\
**CSS3**
스타일 시트 표준, 웹 문서에 글꼴, 색상, 정렬과 각 요소의 배치 방법등과 같은 디자인 요소를 적용하는 데 사용  
\
\
**CSS3의 구성**  
- 선택자(Selector): 스타일 시트를 적용할 대상을 지정
- 속성(Property): 어떤 속성을 적용할지 선택
- 속성값(Value): 속성에 어떤 값을 반영할지 선택
```
h1 { color: blue; font-size: 12px; }
```
- h1 => 선택자  
- color, font-size => 속성  
- blue, 12px => 속성값  