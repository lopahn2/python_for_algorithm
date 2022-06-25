# 컴프리헨션 정리
## 기본
```py
# list
numbers = [x for x in range(10)] # [0, 1, ... ,10]
evenNumbers = [2*x for x in range(1,5)] # [2, 4, ... ,8] 
oddNumbers = [x for x in range(10) if x % 2 == 1] # [1, 3, 5, 7, 9]

# 2차원 List
dp = [[0 for i in range(1001)] for i in range(1001)]

# Dictionary
# CREATE
students = ['철수', '영희', '길동', '순희'] 
dicts_ = { student: 0  for student in students } # {'철수': 0, '영희': 0, '길동': 0, '순희': 0}

# UPDATE
scores = {'철수': 50, '영희': 80, '길동': 90, '순희': 60, '전학생': 100} 
scores = { name: score for name, score in scores.items() if name != '전학생'} 

```

## 딕셔너리의 최대 값 찾기
```py
answer = [k for k, v in alpha.items() if v == max(alpha.values())]
```
