# radix_sort

```python
from collections import deque

def radix_sort(nums):
    buckets = [deque() for _ in range(10)]

    max_val = max(nums)
    Q = deque(nums)
    cur_ten = 1

    while max_val >= cur_ten:
        while Q:
            num = Q.popleft()
            buckets[(num // cur_ten) % 10].append(num)

        for bucket in buckets:
            while bucket:
                Q.append(bucket.popleft())

        cur_ten *= 10

    return list(Q)

print(radix_sort([15, 27, 64, 25, 50, 17, 39, 28]))
```

radix sort란 정수들을 일의 자리부터 비교해서 정렬하는 알고리즘이다. <br>
bucket 이라는 queue 개념을 사용해 정렬하기 때문에 O(n)의 시간복잡도를 가지는 아주 빠른 정렬 알고리즘 <br>

1. 0-9의 숫자들에 대응되는 queue를 buckets에 index(0~9)로 관리
2. 숫자들의 1의자리 숫자로 buckets에 넣음
3. 버켓에 넣은 순서대로 다시 Q에 집어넣음
4. 다음 자리 숫자로 buckets에 넣음
5. Q의 가장 큰 값보다 자리수가 커지면 종료.

이러면 정렬된다.
