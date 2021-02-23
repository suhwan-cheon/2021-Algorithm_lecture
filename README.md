# 2021-Algorithm_lecture
2021년 겨울방학 항공대학교 알고리즘 학회 Koala 기초강의

강의 링크 : https://www.youtube.com/watch?v=ykZZbNCAEJU&list=PLBdD-Necee4nHCmsBQPMmlQz8IYn489zz

## 커리큘럼 정리

### 강의 구성

총 14개의 알고리즘 유형 (주 2회, 총 7주)

유형별 구성

이론 10분

기본 코드 10분

문제 10분 ~ 20분

### **0. 오리엔테이션**

시작 전 알아야할 것들, 알아두면 좋은 것들

- 세부 계획 설명
- 팀블로그 글 올리기
- 백준 그룹 활용
- 슬랙 사용법

+) **정렬**

- C++은 algorithm 헤더 파일에 있는 sort 사용. sort는 배열을 오름차순으로 정렬한다. (문자열도 가능)
- 따로 함수를 만들어 넣으면 정렬 방식을 바꿀 수 있다.
- 특히 직접 struct를 구현하는 경우, 비교 함수를 만들어야 한다.
- 정렬이 이진탐색보다 앞에 와야 하지 않나 싶습니다.(이진탐색을 위해 필요합니다)

### **1.완전 탐색(기본)**

**이론**

- 기본적인 완전 탐색(브루트 포스)의 개념 설명
→ 완전 탐색이란 "모든 경우의 수를 다 해보는 방법"으로 영어로 Brute-Force(무식하게 풀기)라고도 한다.
→ 왜 이런 방법을 사용하는가? 는 컴퓨터의 빠른 계산 능력을 이용해 푸는 방법인데
- 풀면서 고려해야할 단계 (경우의 수 계산 → 모두 만들어 보기 → 답 구하기)
- 제 경우, 알고리즘에 처음 접근할 때 모든 문제를 브루트 포스로 풀려고 했고, 어느정도 배웠을 때는 시간 초과 걱정때문에 브루트포스로 풀 수 있는 문제임에도 브루트포스를 사용하지 않고 멀리 돌아가곤 했습니다. 언제 사용해야할지, 언제 쓰면 안될지를 강의하면 좋을 것 같습니다.

**문제**

- [https://www.acmicpc.net/problem/20410](https://www.acmicpc.net/problem/20410)(추첨상 사수 대작전 Easy)
→ Normal을 보여주면서 시간초과를 보여줘도 좋을 것 같습니다.

### **2. 완전 탐색(백트래킹)**

**이론**

- 완전 탐색(기본)의 한계 → 더 이상 함수 호출이 의미 없는 경우 지적
- 제외하고 진행하는 백트래킹 기법 소개 (트리 모양으로)
- 문제를 많이 풀어줘야 패턴이 보일 듯하다.
- N중 반복문을 돌리기 위한 방법이라고 소개해도 좋을 것 같습니다. (n과 m 문제의 8중 for문)

**코드**

- N-queen 문제를 가지고, check = true → false 의 재귀 과정을 그림으로 표현하기

**문제**

- [https://www.acmicpc.net/problem/15649](https://www.acmicpc.net/problem/15649)(N과 M(1))
→ N과 M 문제의 모음집을 보여주면 좋을 것 같습니다.
- 스타트와 링크 문제
- 부등호 문제
- n- queen 문제

### **3. 다이내믹 프로그래밍**

**이론**

- 기본 개념 → 큰 문제를 작은 문제로 나눠서 푸는 알고리즘
- 필요한 두 가지 속성 (피보나치로 설명)
1. Overlapping Subproblem (큰 문제와 작은 문제는 푸는 방법이 같다)
2. Optimal Substructure (문제의 정답을 작은 문제의 정답에서 구할 수 있다)
- Optimal Substructure 의 특성 때문에 같은 문제는 구할 때마다 정답이 같고, 따라서 이를 어딘가 메모해놓으면 좋다. →Memoization (Tow-Down)
- Bottom-up : 크기가 작은 문제부터 차례대로 → 점점 크게 만든다. (작은 문제부터 풀었기 때문에 큰 문제는 항상 풀 수 있다.)
- 백트래킹 직후에 있으니 탑다운으로 메모이제이션 먼저 설명하는게 좋을것 같습니다.
- 웰노운(lis, lcs, 냅색, 거스름돈, 돌 게임) 문제는 한번씩 모두 다루는게 좋을 것 같습니다.

**문제**

- [https://www.acmicpc.net/problem/1003](https://www.acmicpc.net/problem/1003) (피보나치 함수)
- [https://www.acmicpc.net/problem/2839](https://www.acmicpc.net/problem/2839) (설탕배달 - 이거 풀때 대가리 깨질뻔 했어효)

### 4. 다이내믹 프로그래밍 2 (only 문제)

### 문제 선정

- 12865 평범한 배낭
- 11053 lis
- 5582 lcs
- 9655 돌 게임
- 2225 합분해
- 2016 scpc 1차 예선 2번 - 징검다리

### 5**. 시뮬레이션**

**이론**

- 문제에 모든 과정이 제시되어 그대로 따라 구현하는 문제
- 구조체를 쓸 때 훨씬 깔끔해보일 때가 많음

→ sw 역량 테스트 문제 기반으로 설명

**문제**

### 5.1 투 포인터

### 6**. 해시**

**이론**

- 해시 함수란? 임의의 길이의 데이터를 고정된 길이의 데이터로 매핑하는 함수
- 특정한 배열의 인덱스 값 또는 value 값을 "데이터 값"을 이용해 찾을 수 있다.
- 보통 String 배열 안에서 원하는 String의 위치를 찾으려면 선형시간 O(N) 또는 정렬된 상태에서 O(logN)이 걸리지만, 해시를 사용하면 O(1) 시간만에 위치를 찾을 수 있다.
- 여러 기법들이 있지만, 여기서는 C++ Stl map 만을 사용할 것이다.
- C++ stl map 간단 설명

**문제**

- 1620 나는야 포켓몬 마스터 이다솜
- 9375 패션왕 신해빈
- 1351 무한 수열

### 7**. 이분 탐색**

**이론**

- 정렬된 배열에서 특정 원소값을 찾는 과정 설명 + 시간 복잡도
- 정답이 가능한가? 를 알 수도 있다. (랜선 자르기, 나무 자르기 같은 문제)
- 이진탐색에서 슬라이딩 윈도우를 사용하는 문제를 한번쯤 소개해도 좋을것 같습니다.(어렵지 않은 선에서)
- 이진탐색 파트에서 [l, r], (l, r)처럼 범위 끝점 처리는 한번 다루면 좋을 것 같습니다.
- lower bound, upper bound 라이브러리 설명과 동시에 set과 multiset 사용법도 익히면 좋을 것 같습니다. 마침 해싱 다음이네요.

**기본 코드**

int left = 0, right = n;

while(left ≤ right)

{

int mid = (left + right) / 2;

if(calc(mid)){

ans = mid;

left = mid + 1;

}

else right = mid - 1;

}

**문제**

- 랜선 자르기
- 기타 레슨
- 공유기 설치

### 7.1 upper_bound , lower_bound 사용법

- upper_bound : 찾고자 하는 값보다 같거나 큰 원소가 첫 번째로 나타나는 위치
- lower_bound : 찾고자하는 값보다 큰 원소가 첫 번째로 나타나는 위치
- 조건 : 배열들이 오름차순으로 정렬되어 있어야 한다.
- 이분 탐색(Binary Search) 기반의 구현
- 반환형은 Iterator(반복자) 이므로, 벡터의 경우 실제 인덱스를 알고 싶다면 같은 Iterator v.begin()을 빼주면 된다.

### 8**. 스택**

**이론**

- 스택의 성질을 먼저 알려주고 STL을 사용해서 구현을 하는게 아닌 먼저 스택을 직접 만들어 보면 조금 더 쉽게 이해할 것 같습니다.
- LIFO을 그림으로 설명하면서 (PUSH, POP, TOP, EMPTY 함수와 같이)
- 스택은 한쪽 끝에서만 자료를 넣고 뺄 수 있는 자료구조이다
- 마지막으로 넣은 것이 가장 먼저 나오기 때문에 Last In Frist Out (LIFO) 라고도 한다
- 
- push: 스택에 자료를 넣는 연산
• pop: 스택에서 자료를 빼는 연산
• top: 스택의 가장 위에 있는 자료를 보는 연산
• empty: 스택이 비어있는지 아닌지를 알아보는 연산
• size: 스택에 저장되어있는 자료의 개수를 알아보는 연산

**문제**

- [https://www.acmicpc.net/problem/10828](https://www.acmicpc.net/problem/10828)(스택 - 기본 구현 문제)
- [https://www.acmicpc.net/problem/9012](https://www.acmicpc.net/problem/9012)(괄호 - 스택 응용 문제)
- [https://www.acmicpc.net/problem/1874](https://www.acmicpc.net/problem/1874)(스택 수열 - 스택 응용 문제)
- [https://www.boj.kr/1406](https://www.boj.kr/1406) (에디터 - 스택 응용 문제)

### 9**. 큐, 덱**

**이론**

- 이론은 쉬운데... 떠올리기가 어려운 문제 같습니다. 설명은 간단히, 문제를 많이 풀려봐야 할 것 같습니다
- 큐와 덱의 성질을 먼저 알려주고 STL을 사용해서 구현을 하는게 아닌 먼저 큐와 덱을 직접 만들어 보면 조금 더 쉽게 이해할 것 같습니다.
- FIFO을 그림으로 설명하면서 (PUSH, POP, FRONT, EMPTY 함수와 같이)
- 우선순위 큐도 알려줄까요? 우선큐도 해야죠 나 문제풀면서 우선큐 사용한 문제가 더 많았던것 같아 일단 큐를 기본적으로 이해하면 우션큐는 어차피 쉬우니까

**문제**

- [https://www.acmicpc.net/problem/1158](https://www.acmicpc.net/problem/1158) (요세푸스 문제)
- [https://www.acmicpc.net/problem/18258](https://www.acmicpc.net/problem/18258) (큐2 - 기본 구현 문제)
- [https://www.acmicpc.net/problem/10866](https://www.acmicpc.net/problem/10866) (덱 - 기본 구현 문제)
- [https://www.acmicpc.net/problem/1406](https://www.acmicpc.net/problem/1406) (에디터 -덱 응용)

### 9.1 우선순위 큐

11장 다익스트라에 대한 사전 지식으로 우선순위 큐는 필수이기 때문에 중간에 추가하였습니다.

**이론**

- 우선순위 큐 그 자체인 힙에 대해 설명을 해주어야겠지요
- c++ stl을 이용해 우선순위 큐(max, min heap) 을 어떻게 만드는지만 보여줄 생각입니다. (직접 구현까지 안하고)

**문제**

- 13975 파일합치기 3
- 7662 이중 우선순위 큐
- 1477 휴게소 세우기

### 10**. 그래프(bfs/dfs)**

**이론**

- 그래프 기본 개념 설명(정점과 간선, 경로와 사이클, 간선의 방향, 가중치, 차수)
- 그래프의 표현 방식 (인접 행렬과 인접 리스트)
- 깊이 우선 탐색은 재귀 호출을 이용해 구현 가능
- 너비 우선 탐색은 큐를 이용해 구현 가능
- 코딩테스트에서 플러드 필 문제가 많이 나옵니다. 여러 형태로 두세문제 넣어도 좋을 것 같습니다.

**문제**

- [https://www.acmicpc.net/problem/1260](https://www.acmicpc.net/problem/1260) (DFS와 BFS - 생 구현 문제)
- [https://www.acmicpc.net/problem/1012](https://www.acmicpc.net/problem/1012) (문제 이해도 쉽고 직관적인 문제네요. 실제로 풀이과정을 보여주면 좋을 것 같습니다)
- [https://www.acmicpc.net/problem/2468](https://www.acmicpc.net/problem/2468) (안전영역 - 간단한 로직이 추가된 문제)
- [https://www.acmicpc.net/problem/2206](https://www.acmicpc.net/problem/2206) 벽 부수고 이동하기 - BFS, DFS의 응용문제로 이런 문제도 있다는 것을 알려주면 좋을 것 같습니다. 비슷한 문제로 ([https://www.acmicpc.net/problem/1600](https://www.acmicpc.net/problem/1600)) 말이 되고픈 원숭이

### **11. 다익스트라**

**이론**

**문제**

### **12. 트리**

**이론**

- 기본 이론 설명(트리의 구성 방식)
- 순회 방식 설명(전위, 중위, 후위 순회)
- 사실... 트리가 어떤건지도 알고 대충 구현할줄도 아는데 문제에 적용시키기 어려운것 같아요... 문제 구현 중심적인 설명도 있으면 좋을 것 같습니다.

**문제**

- [https://www.acmicpc.net/problem/1991](https://www.acmicpc.net/problem/1991) (트리 순회 - 트리를 전위,중위,후위순회하는 문제)

### **13. 위상정렬**

**이론**

**문제**

### **14. 그리디**

**이론**

- 문제 예시를 통해서 설명하는 것이 가장 좋을 것 같습니다. 이인복 교수님의 강의 자료 문제를 이용해서 설명해도 좋을 것 같습니다. 강의실 배정!!

**문제**

- [https://www.acmicpc.net/problem/1931](https://www.acmicpc.net/problem/1931) (이인복 교수님의 Pick)
