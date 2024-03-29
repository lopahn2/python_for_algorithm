
# 문자열 정리

## 문자열 인덱싱
```python
string_ = "hello"

string_[0:2] # he
len(string_) # 5

# 슬라이싱
string[여기서부터 : 여기전까지 : 이만큼간격으로 가져와줘요]

>>> a = ['a', 'b', 'c', 'd', 'e']
# 2칸씩 이동하면서 가져옵니다.
>>> a[ : : 2 ]
['a', 'c', 'e']


>>> a = ['a', 'b', 'c', 'd', 'e']
# 3칸씩 이동하면서 가져옵니다.
>>> a[ -5 : : 3 ]
['a', 'd']


>>> a = ['a', 'b', 'c', 'd', 'e']
# 전체를 거꾸로 가져옵니다.
>>> a[ : : -1 ]
['e', 'd', 'c', 'b', 'a']


>>> a = ['a', 'b', 'c', 'd', 'e']
>>> a[ 3 : : -1 ]
['d', 'c', 'b', 'a']
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

## 문자 찾기
### find(찾을문자, 찾기시작할위치)
```python
>>> s = '가나다라 마바사아 자차카타 파하'
>>> s.find('마')
5
>>> s.find('가')
0
>>> s.find('가',5)
-1
```
find는 문자열중에 특정문자를 찾고 위치를 반환해준다, 없을경우 -1을 리턴 <br>
### startswith(시작하는문자, 시작지점)
```python
>>> s = '가나다라 마바사아 자차카타 파하'
>>> s.startswith('가나다')
True
>>> s.startswith('마')
False

>>> s.startswith('마',s.find('마')) #find는 '마' 의 시작지점을 알려줌 : 5
True
>>> s.startswith('마',1)
False
```
startswith는 문자열이 특정문자열로 시작하는지 여부를 알려준다 <br>
두번째 인자를 넣음으로써 찾기시작할 지점을 정할수있다. <br>

### endswith(끝나는문자, 문자열의시작, 문자열의끝)
```python
>>> s = '가나다라 마바사아 자차카타 파하'
>>> s.endswith('마')
False
>>> s.endswith('하')
True

>>> s.endswith('마',0,10)
False
>>> s.endswith('마',0,6)
True
```
endswith는 문자열이 특정문자로 끝나는지 여부를 알려준다.
