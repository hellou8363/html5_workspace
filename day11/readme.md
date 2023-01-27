## Study Record
\
**position(fixed, sticky) 실습**  

\
**float**  
화면을 구성하는 요소 간의 관계를 고려하여 각 요소를 배치하는 방법  
(예: 이미지와 글을 어울리게 배치할 때, 갤러리(여러 이미지 나열) 만들 때)  
- inherit: 요소를 감싸는 부모 요소의 float 속성을 상속받음
- left: 요소의 왼쪽으로 떠 있는 상태로 설정
- right: 요소의 오른쪽으로 떠 있는 상태로 설정
- none: float 속성 적용 X(요소를 떠 있게 하지 않음)  

\
float가 지정되면 다음 요소도 float가 지정된다.  
만약, float: left;이면, 다음 요소도 float: left;가 적용된다.  
\
clear: float속성값; => float 속성이 적용되지 않도록 할 때 사용  
```
clear: both; /* left, right에 관계없이 float 속성 적용 X */
```  
\
overflow: auto; => 이미지가 박스 영역을 벗어나는 현상 해결  
자식 요소가 부모 컨테이너 영역을 넘을 때, 자식 요소의 높이를 다 포함할 만큼 부모 컨테이너가 자동으로 늘어난다.  
