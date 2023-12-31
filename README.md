# COSPro
**1차 1번** (추상클래스)
 - 추상메소드 구현
 - https://dojang.io/mod/page/view.php?id=2389
 - 일반적이므로 메서드를 정의할 때 self 를 첫번째 인자값으로 주는 것이 좋음

   
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

 __ __ __ __ __ __ __
 **4차 5번**
 - 문자열 뒤집기
   - string [::-1]
   - reversed(string)
  
 **4차 6번**
 - 정수 자리수 분리
   - ```python
     while current != 0:
     current % 10    <- 맨 뒤에서부터 한자리씩
     current=current//10
     ```
**4차 8번**
- 파이썬 배열 중복 요소 제거 : set(리스트) 하고 다시 list(리스트)로 감싸기
  
**4차 9번**
- 시계의 각도 계산
  
  시침 : 한시간에 30도, 1분에 0.5도
  분침 : 한시간에 360도, 1분에 6도
    
  ex) 4시 30분
  abs(4* 40 + 30* 0.5 - 30*6)

 __ __ __ __ __ __ __
 **5차 6번**
- 진법변환 :  https://velog.io/@code_angler/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EC%A7%84%EC%88%98%EB%B3%80%ED%99%982%EC%A7%84%EB%B2%95-3%EC%A7%84%EB%B2%95-5%EC%A7%84%EB%B2%95-10%EC%A7%84%EB%B2%95n%EC%A7%84%EB%B2%95
- n진수 -> 10진수 : int(string, base)
- 10진수 -> n진수 :
```python
def solution(number, q):
    rev_base = ''

    while number > 0:
        number, mod = divmod(number, q) -> 몫이랑 나머지 같이 구함 
        rev_base += str(mod)

    return rev_base[::-1] 
```
**5차 7번**
- 사이클 찾기 : https://velog.io/@yujin1760/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98Union-Find-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98
- 1. 각 노드의 부모 노드를 자기자신의 노드번호로 초기화
  2. 재귀적으로 부모노드찾기
  3. union으로 부모 합치기
  4. find로 두 노드가 같은 parent를 가지는지 판별

- 배열 번호로 배열 초기화 :  [i for i in range(n+1)]

 __ __ __ __ __ __ __
 **6차 1번**
 - 2차원 배열 생성 : [[0 for i in range(n)] for j in range(n)]
 - deque사용법 : from collections import deque, q=deque()
