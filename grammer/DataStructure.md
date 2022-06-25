# 자료구조 정리
## Deque
```py
from collections import deque 
queue = deque() 

queue.popleft() # 디큐의 전단을 삭제 
queue.pop() # 디큐의 후단을 삭제 
queue.append('data') # 디큐의 후단에 데이터 삽입 
queue.appendleft('data') # 디큐의 전단에 데이터 삽입 

queue.extend('abc') # queue >> [a, b, c]  # deque에 iterable argument(list, str, tuple...)를 분리해서 append 해주는 메서드. 
queue.extendleft('def') # queue >> [f, e, d, a, b, c]  # deque에 iterable argument(list, str, tuple...)를 분리해서 appendleft 해주는 메서드. 

queue.rotate(n) # queue의 값들을 n 값 만큼 회전시켜주는 메서드. 양수면 오른쪽, 음수면 왼쪽으로 회전
```

