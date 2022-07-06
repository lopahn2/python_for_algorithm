
# 리스트 정리
## 인덱싱
```py
numbers = [2, 3, 4, 5, 6]
numbers[1:4] # [3, 4, 5] [여기부터 : 여기전까지]
```

## CRUD
```py
numbers = [1, 2, 3, 4]

len(numbers) # 4

numbers.append(5) # [1, 2, 3, 4, 5]
numbers.extend([6, 7, 8]) # [1, 2, 3, 4, 5, 6, 7, 8]

del numbers[numbers.index(8)] # [1, 2, 3, 4, 5, 6, 7]
# list.index(value) => value's index

numbers.insert(numbers.index(4), 3.5) # [1, 2, 3, 4.5, 4, 5, 6, 7]

overlaps = [1, 2, 2, 2, 3, 4]
overlaps.remove(2) # [1, 2, 2, 3, 4]
# 첫 번째로 값을 가지는 데이터를 삭제
```

## 정렬
```py
numbers = [4, 3, 6, 2, 1, 7]
tuples = [(1, 2), (3, 4)]

new_list = sorted(numbers, reverse = True) # 내림차순 정렬 기본값 reverse = False - 오름차순

new_list = sorted(tuples, key = lambda x : (x[0], -x[1])) # 튜플의 첫 번째로 오름차순 정렬하다가 같은 값이면 두 번째로 내림차순 정렬

numbers.sort(reverse = False) # numbers 배열 자체를 오름차순으로 정렬

numbers.reverse() # 리스트 뒤집기 [7, 1, 2, 6, 3, 4]
```

## 값  찾기
```py
prime = [2, 3, 5, 7, 11]
if 2 in prime:
	print(2 + ' is in prime')
if 6 not in prime:
	print(6 + ' is not in prime')
```

## 리스트 출력
```py
array = ['a', 'b', 'c']

# 리스트를 공백으로 구분하여 출력
' '.join(array) # 'a b c' 
```

## 중복 제거
```py
strList = ['a', 'a', 'aa', 'a', 'b']

# 순서는 그대로 둔 채 리스트 중복 제거
strList = list(dict.fromkeys(strList))
# 순서 신경 안쓰고 리스트 중복 제거
strList = list(set(strList))
```

## ZIP 함수
`zip()`  함수는 여러 개의 순회 가능한 객체를 인자로 받고, 각 객체가 담고 있는 원소를 tuple의 형태로 차례로 접근할 수 있는 반복자를 반환한다.

```py
>>> numbers = [1, 2, 3]
>>> letters = ["A", "B", "C"]
>>> for pair in zip(numbers, letters):
...     print(pair)
...
(1, 'A')
(2, 'B')
(3, 'C')
```

### 다시 분리하기!
```py
>>> numbers = (1, 2, 3)
>>> letters = ("A", "B", "C")
>>> pairs = list(zip(numbers, letters))
>>> print(pairs)
[(1, 'A'), (2, 'B'), (3, 'C')]
```

### 딕셔너리에 활용
```py
>>> keys = [1, 2, 3]
>>> values = ["A", "B", "C"]
>>> dict(zip(keys, values))
{1: 'A', 2: 'B', 3: 'C'}
```

## enumerate 함수
```py
lst = ['a','b','c','d']
for i, k in enumerate(lst):
    print(i,k)

(0,'a')
(1,'b')
(2,'c')
(3,'d')
```

## 자주 쓰이는 함수
```py
#### 문자의 개수 찾기
countList = [1,2,2,3,3,3]
countList.count(1) # 1
countList.count(2) # 2
countList.count(3) # 3

#### 문자열과 숫자 구분하는 함수
text1 = 'abcd' 
text1.isalpha() # True 
text2 = 1234 
text2.isalnum() # True

#### 값을 순회할 때 조건을 걸고 싶을 때
string = '0001100' 
res = list(filter(lambda x: string[x]=='0', range(len(string)))) # [0, 1, 2, 5, 6]

#### itertools
items = ['1', '2', '3', '4', '5'] 

# 중복 허용할 때! (순열)  
from itertools import permutations 
list(permutations(items, 2)) # [('1', '2'), ('1', '3'), ('1', '4'), ('1', '5'), ('2', '1'), ('2', '3'), ('2', '4'), ('2', '5'), ('3', '1'), ('3', '2'), ('3', '4'), ('3', '5'), ('4', '1'), ('4', '2'), ('4', '3'), ('4', '5'), ('5', '1'), ('5', '2'), ('5', '3'), ('5', '4')] 

# 중복 허용하지 않을 때! (조합)  
from itertools import combinations 
list(combinations(items, 2)) # [('1', '2'), ('1', '3'), ('1', '4'), ('1', '5'), ('2', '3'), ('2', '4'), ('2', '5'), ('3', '4'), ('3', '5'), ('4', '5')]
```
