
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
