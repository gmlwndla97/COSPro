# COSPro
**1차 1번** (추상클래스)
 - 추상메소드 구현
 - https://dojang.io/mod/page/view.php?id=2389

   
**1차 5번** (재귀, 탐색)
 - 재귀 :  https://whatryando.tistory.com/125
- bfs 탐색

   
   
**1차 6번**
- mxn 배열 만들기
  - ``` arr=[[0]*(m) for _ in range(n)]```
 __ __ __ __ __ __ __
**2차 1번** (추상클래스)
- 추상클래스 메소드명, parameter 모두 동일하게 상속받아야 함

**2차 2번** (단순구현)
- XX:YY 형태의 시간 비교 -> 분으로 환산
  - ```python
     def func_a(times):
	     hour = int(times[:2])
	     minute = int(times[3:])
      	return hour*60 + minute
    ```
**2차 4번** (조합)
- 조합 구하기
  - combinations
    - ```python
      from itertools import combinations
      comb=combinations(arr, 3)
      comb=list(comb)
      ```
  - 중첩 for문
 	- ```python
	    for p in range(0, n):
	      for q in range(p + 1, n):
    		for r in range(q + 1, n):
    	 ```
       
      
**2차 5번** (DP)
- 가장 긴 증가하는 부분수열(LIS)
  - DP  : O(n^2)
  	- ```python
    	 for i in range(0, len(arr)-1) :
        	if(arr[i]<arr[i+1]):
            	dp[i+1]=dp[i]+1
    	```
  - 이진탐색 lower bound : O(nlongn)

**2차 6번** (단순구현)
- 파이썬에서는 문자열과 for문을 같이 쓰면  한 글자씩 따로 접근가능

**2차 7번** (거스름돈 그리디)

 __ __ __ __ __ __ __
**3차 2번** (완전탐색)
- 2중 for문
   - ```python
     ```
- 참고) cos pro 2급 팰린드롬 판단하기
