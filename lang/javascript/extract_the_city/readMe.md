# Extract the city - 19. 01. 28

이 문제는 입력값을 사용하여 출력값의 형태로 변형한다.

- 기본 함수
  - concatSecondDiagonal
    - 파라미터
      - twoDimArray : 배열
        - 2차원 배열을 인자로 받는다.

- 입력 <br>
  <pre> 
  [
    ['a','z','x','C','v','B'],
    ['t','w','I','p','e','7'],
    ['w','y','o','r','m','x'],
    ['q','U','l','s','k','H'],
    ['A','i','G','Y','h','L'],
    ['n','f','d','W','z','a']
  ] </pre>
 
- 출력 <br>
   <pre>  "Berlin" </pre>

<br>

- 추가함수
  - 없음

> 문제
  - 주어진 배열에서 도시 이름을 찾는다.
  - 찾는 방법은 각 배열에서 도시의 이름을 맞추기위해 한 자씩 꺼낸다.
    - 첫번째 배열에서는 첫번째배열의 가장 마지막값을 꺼내고, 그 이후부터는 하나씩 인덱스를 앞당겨서 꺼낸다.
    - ex) 위의 입력에서 
      - 첫번째 : 가장 마지막에 있는 요소 => B를 꺼낸다.
      - 두번째 : 가장 마지막에서 한 칸 앞에 있는 요소 : e를 꺼낸다.
      - 세번째 : 가장 마지막에서 두 칸 앞에 있는 요소 : r을 꺼낸다.

> 설명
  - 가장 마지막값은 해당 배열의 끝(length-1)이므로 현재 인덱스에 해당하는만큼 값을 빼서 원하는 값을 꺼낸다.