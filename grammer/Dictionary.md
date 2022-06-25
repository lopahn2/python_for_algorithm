# 딕셔너리 정리
## CRUD
```py
my_dic = { 
'a': 25, 
'b': 4, 
'c': 9 }

# READ
my_dic['a'] # 25
my_dic.get('b', -1) # key = b 인 value가 있으면 value를, 없으면 지정값(-1)을 불러옴

# CREATE
my_dic['d'] = 16

# UPDATE
my_dic['d'] = 15

# DELETE
# del 이용하기 - 키가 있는 경우  
dict = {'김철수': 300, 'Anna': 180} 
del  dict['김철수'] 
dict  #{'Anna': 180}

# del 이용하기 - 키가 없는 경우 raise KeyError 
my_dict = {'김철수': 300, 'Anna': 180} 
del my_dict['홍길동'] 
'''
keyError 발생! 
'''

# pop 이용하기 - 키가 있는 경우 대응하는 value 리턴
my_dict = {'김철수': 300, 'Anna': 180}
my_dict.pop('김철수', 180) # 300

# pop 이용하기 - 키가 없는 경우 대응하는 default 리턴 
my_dict = {'김철수': 300, 'Anna': 180} 
my_dict.pop('홍길동', 180) # 180

# key가 딕셔너리에 있는지 확인
dict = {'김철수': 300, 'Anna': 180} 
print("김철수"  in  dict) #True  
print("김철수"  not  in  dict) # False

# 순회
for value in my_dic.values():
	print(value) # 25 -> 4 -> 9 -> 15
for key in my_dic.keys():
	print(key) # 'a' -> 'b' -> 'c' -> 'd'
for key, value in my_dic.items():
	print(key, value)
```

## 해싱
```py
check_hash = {}

for member in mebers:
	check_hash[hash(member)] = member
```
파이썬 내장 hash 함수로 값을 해싱할 수 있고 이는 특정 값을 고유한 숫자로 표현할 때 사용한다. 

