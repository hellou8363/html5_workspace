## Study Record
\
**border**  
박스 테두리의 두께로 border-top, border-bottom과 같이 각 테두리에 개별 스타일 적용 가능  
\
\
**border-style**  
테두리 스타일 설정
- none: 기본값, 테두리가 나타나지 않음
- hidden: 테두리를 감춤
- dotted: 점선으로 지정
- dashed: 파선으로 지정
- solid: 실선으로 지정
- double: 이중선으로 지정
- groove: 오목한 선으로(홈이 파인듯 입체적으로) 지정
- ridge: 볼록한 선으로(튀어나온 듯 입체적으로) 지정
- inset: 테두리의 안쪽을 오목한 선으로 지정
- outset: 테두리의 안쪽을 볼록한 선으로 지정

\
**border-width**  
테두리 두께 설정(top, bottom, left, right)
- 수치: 테두리의 두께를 픽셀(px), 포인트(pt), 센티미터(cm) 같은 단위로 지정
- thin: 얇은(1px) 두께의 테두리를 지정
- medium: 기본값, 중간(3px) 두께의 테두리를 지정
- thick: 굵은(5px) 두께의 테두리를 지정

\
**border-radius**  
테두리의 모서리를 둥글게 설정
- ```border-radius```: 속성값; => 네 개의 모서리를 모두 둥글게
- ```border-top-left-radius```: 속성값; => 상단 왼쪽 모서리를 둥글게
- ```border-top-right-radius```: 속성값; => 상단 오른쪽 모서리를 둥글게
- ```border-bottom-right-radius```: 속성값; => 하단 오른쪽 모서리를 둥글게
- ```border-bottom-left-radius```: 속성값; => 하단 왼쪽 모서리를 둥글게  


=> radius의 속성값이 요소의 가로, 세로 길이의 1/2값이면 원 모양이 된다.  
\
\
**box-shadow**  
박스에 그림자 효과 적용  
``` 
{ box-shadow: 수평 그림자(필수) | 수직 그림자(필수) | 그림자 흐림 | 그림자 번짐 | 그림자 색상 | 삽입효과; }
```
- 수평 그림자(h-shadow): 그림자의 수평 거리 지정
- 수직 그림자(v-shadow): 그림자의 수직 거리 지정
- 그림자 흐림(blur): 그림자의 흐림 정도 지정
- 그림자 번짐(spread): 그림자의 번짐 정도 지정
- 그림자 색상(color): 그림자의 색상 지정
- 삽입 효과(inset): 박스 외부로 표현되는 그림자를 박스 안쪽으로 표현하는 효과

\
**Layout 속성**  
- position
- float
- z-index
- display

\
**위치 속성**  
- top: viewport의 원점에서 위쪽 끝에서, 얼마나 떨어져 있는지 나타내는 값
- left: viewport의 원점에서 왼쪽 끝에서, 얼마나 떨어져 있는지 나타내는 값
- right: viewport의 원점에서 오른쪽 끝에서, 얼마나 떨어져 있는지 나타내는 값
- bottom: viewport의 원점에서 아래쪽 끝에서, 얼마나 떨어져 있는지 나타내는 값

\
하나의 요소 위치를 결정할 때는 아래와 같이 쌍으로 지정하여 사용  
- top / left
- top / right
- bottom / left
- bottom / right

\
**웹브라우저의 viewport 영역**  
- 좌측 상단(Left-Top)이 원점(0, 0)
- X축은 그대로, Y축은 아래로
- Z축은 viewport를 보는 화자의 방향으로 나온다.

\
**position**  
텍스트, 이미지, 표 등의 요소를 웹 문서에 배치할 때 사용하는 속성  
- ```position: static;``` => 정적 위치 설정, 각종 요소를 웹 문서의 흐름에 따라 배치  
  (블록 요소는 위에서 아래로 쌓이고, 인라인 요소는 같은 줄에 순서대로 배치되며 top, right, bottom, left 위치 속성 적용 X )
- ```position: relative;``` => 상대 위치 설정, 웹 문서의 정상적인 위치에서 상대적으로 얼마나 떨어져 있는지 표시하여 배치하는 방법  
  (중요!! => 상대위치설정은 위치를 변경시키는 용도로는 거의 사용되지 않고, 자식요소 중 ```position: absolute```속성을 가진 요소의, 기준점이 되는 부모요소가 되기 위해 ```position: relative```속성을 가지거나 body태그를 기준점으로 삼음)
- ```position: absolute;``` => 절대 위치 설정, 전체 페이지를 기준으로 top, right, bottom, left의 속성을 이용하여 원하는 위치에 배치하는 방법
- ```position: fixed;``` => 고정 위치 설정, 요소의 위치를 '절대 위치 설정'과 똑같은 방법으로 배치하되, 창의 스크롤을 움직여도 사라지지 않고 고정된 위치에 그대로 있음
- ```position: sticky;``` => 고정 위치 지정, 가장 가까운 스크롤 조장이 뷰포트일 때, 상대 위치 지정과 고정 위치 지정의 하이브리드
- ```position: initial;``` => static과 동일
- ```position: inherit;``` => 부모 요소의 position속성으로부터 상속받음
