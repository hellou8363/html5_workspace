## Study Record
\
**Emmet Code를 활용한 태그 완성**  
참고링크: https://docs.emmet.io/abbreviations/syntax/  
\
**사용자정의 태그 및 속성**  
사용자정의 태그와 속성은 브라우저가 인식할 수 없으므로 렌더링에서 무시된다.  
다만, 태그 내 컨텐츠는 그대로 출력된다.  
\
**태그의 속성**  
- 태그의 종속적인 정보를 표현하기 위해 사용  
- 태그없이 단독으로 사용할 수 없음  
- 속성="값" 형태로 작성  
```
<시작태그 속성="값"></끝나는태그>
```  
\
**Markup Language 구현수단: "태그"의 2가지 종류**
1. Pre-defined Tags: HTML5 표준에 정의된 태그로 렌더링 대상이 된다.  
    가. Pre-defined Attributes: 미리 정의된 속성  
    나. User-defined Attributes: 사용자정의 속성도 함께 사용가능   
    다. Global Attributes: 전역 속성(모든 태그에서 공통으로 사용가능한 속성)  
    라. Event Attribues: 이벤트 속성(모든 태그에서 공통으로 사용가능한 속성)
2. User-defined Tags: 개발자가 임의로 정의한 태그로 렌더링 대상에서 제외 된다.  
    가. User-defined Attributes: 사용자정의 속성  
    나. Global Attributes: 전역속성(모든 태그에서 공통으로 사용가능한 속성)  
    다. Event Attribues: 이벤트 속성(모든 태그에서 공통으로 사용가능한 속성)  

\
\
**```<a href="#">```을 이용한 책갈피 기능**: sample7.html  
\
\
**웹 문서의 레이아웃**  
- 화면을 분할하거나 배열하여 구성하는 것  
- HTML5 웹 표준에서는 각 영역을 구분하는 구조적 태그 요소를 정의하여 사용  

```<header>```: HTML5 문서의 머리말 영역으로 중요한 정보를 표시(예: 사이트의 제목, 로고 등)  
```<nav>```: 내비게이션(navigation) 영역으로 웹 사이트 내에서 분류된 다른 영역으로 이동할 때 사용  
```<section>```: 문서의 영역을 구성할 때 사용하며 ```<header>```, ```<article>``` 태그 등을 포함할 수 있음  
```<article>```: 독립된 주요 콘텐츠 영역을 정의, 하나의 ```<section>``` 태그 내에 여러 개의 ```<article>``` 태그를 구성할 수 있음  
```<aside>```: 주요 콘텐츠 이외에 남은 콘텐츠를 표시(예: 사이드 바(sidebar) 등)    
```<footer>```: 사이트의 자세한 정보를 표시(예: 저작권 정보, 관리자 정보, 회사 정보 등)  
\
\
**Lorem Picsum(Zafer AYAN) 확장 설치**  
무작위 이미지를 지정한 사이즈에 맞게 넣어준다.