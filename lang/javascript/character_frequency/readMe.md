# Character frequency - 19. 10. 10

이 문제는 입력값을 출력값의 형태로 만들어 반환한다.

- 기본 함수 (1)
  - letterFrequency(text:문자열)
    - 결과값 출력
- 기본적으로 주어지는 객체(0)
- 문제에서 요구하는 다른 함수(0)
- 추가함수(2)
  - sort(arr: 배열)
    - 문제에서 지정하는 대로 해당 배열을 정렬하는 함수
  - range(start: 정수, end: 정수)
    - Array.prototype에 지정한 함수. 다른 문제풀이에 썼던 함수를 그대로 가져옴.
    - start부터 시작해서 end까지 지정한 작업을 수행한 후 수행한 결과를 배열로 반환한다.
- 추가클래스(0)
- 추가객체(0)

- 입력
  <pre> 'wklv lv d vhfuhw phvvdjh' </pre>
 
- 출력
  <pre> [['v', 5], ['h', 4], ['d', 2], ['l', 2], ['w', 2], ['f', 1], ['j', 1], ['k', 1], ['p', 1], ['u', 1]] </pre>

> 문제
  - 이 문제는 주어진 문자열을 사용하여 결과값을 반환한다.
  - 해당 문자열에서 특수문자를 제외한 알파벳만을 기준으로 각 알파벳 문자마다 나타나는 횟수를 구한 후 그 값을 사용하여 가장 큰 값부터 결과 배열의 가장 앞에 나오도록 정렬한다.
  - 만약 나타나는 횟수가 동일한 경우, 그 횟수에서는 알파벳 순서대로 나오도록 정렬한다.
    - ex) i:7, a:3, c:3, e:2, b:2인 경우의 결과 : [[i, 7], [a, 3], [c, 3], [b, 2], [e, 2]]
  - 대문자는 사용하지않고 소문자만 사용한다. (대문자는 소문자로 만든  후 사용한다.)

> 풀이
  - 정규식을 사용하여 알파벳만을 구한 후 대문자가 포함되었을 경우를 생각하여 소문자로 만든다.
  - a부터 z까지 돌아보며 사용된 알파벳 문자와 그 횟수를 구한다.
    - 사용되지않은 알파벳 문자는 횟수를 배열에 추가하지않는다. (기준은 length로 하였고 해당 length의 길이가 0인 경우, 사용되지않은 알파벳 문자로 판단함.)
  - 횟수를 구한 후 문제에서 지정하는 대로 정렬을 수행한다.
    - 기준은 다음과 같다.
      - 1) 현재 문자의 출현횟수가 다음 문자의 출현횟수보다 적은 경우 : 다음 문자와 현재 문자의 위치를 서로 바꾼다.
      - 2) 현재 문자의 출현횟수와 다음 문자의 출현횟수가 같은 경우 : 현재 문자와 다음 문자 중 어느 문자가 알파벳상으로 먼저 출현하는 지 비교한 후 먼저 출현하는 문자를 앞에 둔다.
        - 정렬 순서는 a, b, c, d, ... , y, z처럼 순방향임.

>변경 이력
