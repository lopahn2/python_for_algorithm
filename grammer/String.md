
# 문자열 정리

## 문자열 인덱싱
```python
string_ = "hello"

string_[0:2] # he
len(string_) # 5
```

## 문자열 찾기
```py
string = "My favorite song is snowman by sia"  
# find  
# 찾는 문자열이 처음 나오는 위치 리턴  
# 없을 경우 -1 리턴  
string.find("is") # 17 
string.find("maroon") # -1 

# 해당 문자열의 개수를 리턴  
string.count("i") # 3 
string.count("maroon")# 0 
```

## strip함수
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

## split, join 함수
```python
my_string = "1. 2. 3. 4." 
my_string.split(".") 
# 문자열을 . 을 기준으로 리스트로 만듬. ['1', ' 2' , ' 3', ' 4'] 
# 화이트스페이스로 구분하고 싶을 시, 파라미터를 안넘겨주면 됨 
my_string = "1 2 3 4" 
my_string.split() # ['1', '2', '3', '4']


li = ["apple", "banana", "kiwi", "tomato"]
# 결합(리스트를 문자열로 결합)  
# 문자열.join(리스트) - 리스트 원소 사이에 문자열을 삽입  

# 공백을 삽입  
" ".join(li) # apple banana kiwi tomato  

# ,를 삽입  
",".join(li) # apple,banana,kiwi,tomato  

li = [1, 2, 3, 4] 
# 리스트의 원소는 모두 str 타입이어야 한다. 아닐경우 오류발생  
" ". join(li)  # 오류발생!  
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
