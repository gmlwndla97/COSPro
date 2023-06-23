# COSPro
**1차 1번**
 - 추상메소드 구현
 - https://dojang.io/mod/page/view.php?id=2389

   
**1차 5번**
 - 재귀 :  https://whatryando.tistory.com/125
- bfs 탐색

   
   
**1차 6번**
- mxn 배열 만들기
  - ``` arr=[[0]*(m) for _ in range(n)]```
 
**2차 1번**
- 추상클래스 메소드명, parameter 모두 동일하게 상속받아야 함

**2차 2번**
- XX:YY 형태의 시간 비교 -> 분으로 환산
  - ``` def func_a(times):
 	hour = int(times[:2])
	 minute = int(times[3:])
	 return hour*60 + minute
    ```
**2차 4번**
- 조합 구하기
  - combinations
    - ``` from itertools import combinations
          comb=combinations(arr, 3)
	  comb=list(comb)
	```
  - 중첩 for문
 	- ```  for p in range(0, n):
        for q in range(p + 1, n):
            for r in range(q + 1, n):
    ```
