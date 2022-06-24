# 딕셔너리 정리
## CRUD
```py
my_dic = { 
'a': 25, 
'b': 4, 
'c': 9 }

# READ
my_dic['a'] # 25

# CREATE
my_dic['d'] = 16

for value in my_dic.values():
	print(value) # 25 -> 4 -> 9 -> 16
for key in my_dic.keys():
	print(key) # 'a' -> 'b' -> 'c' -> 'd'
for key, value in my_dic.items():
	print(key, value)



```
