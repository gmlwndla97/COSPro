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
     for start_idx in range(length):
	     for cnt in range(1, length - start_idx + 1):
		     sub_s = s[start_idx : start_idx + cnt]
       
       for i in range(length // 2):
		if s[i] != s[length - i - 1]:
			return False
       return True
     ```
- 참고) cos pro 2급 팰린드롬 판단하기

**3차 3번** (완전탐색)
- dx, dy 활용

**3차 4번** (문자열 슬라이싱)
- s2[-i:] = 맨뒤에 i개 성분을 선택하는 것

**3차 6번** (소수판별)
- 에라토스테네스의 체
- ```python
  for i in range (3, n + 1, 2) :
  	is_prime = True
	for j in range(2, i) :
		if i % j == 0 :
		is_prime = False
		break
	if is_prime==True:
		primes.append(i)
  ```
**3차 9번**
- 인덱스 한줄 수정
