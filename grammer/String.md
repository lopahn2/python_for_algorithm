# 문자열 정리

## 문자열 인덱싱
```python
string_ = "hello"

string_[0:2] # he
len(string_) # 5
```

## strip 함수
```python
string_ = "   abc   dfe   "
new_string = string_.strip()
# "abc   dfe" 
# 맨 앞과 맨 뒤의 화이트 스페이스가 사라짐
# 화이트 스페이스란 " " , "\t", "\n" 등.

strip('.') # 양 끝의 . 을 삭제
rstrip('.') # 오른쪽 끝의 . 을 삭제
lstrip('.') # 왼쪽 끝의 . 을 삭제
```

## split 함수
```python
my_string = "1. 2. 3. 4." 
my_string.split(".") 
# 문자열을 . 을 기준으로 리스트로 만듬. ['1', ' 2' , ' 3', ' 4'] 
# 화이트스페이스로 구분하고 싶을 시, 파라미터를 안넘겨주면 됨 
my_string = "1 2 3 4" 
my_string.split()​ # ['1', '2', '3', '4']
```

## replace 함수
```python
text_str = "안녕하세요 저는 화니에요" 
text_str.replace(" ", "") # 안녕하세요저는화니에요​
```

## 대문자 소문자
```py
'hello'.upper() # HELLO
'HELLO'.lower() #hello

'S'.isupper() # True
'T'.islower() # False
```

## 알파벳 숫자
```py
string_.isalpha() # 알파벳이면 True
string_.isdigit() # 숫자면 True
```
