# 함수 정리

## 진수 변환

```py
# bin(number) => number를 binary 문자열로 변환한다.
# 결과값은 0b를 붙여 나오므로 문자열 슬라이싱을 진행한다.

# 사용 예시
def solution(n, arr1, arr2):
    # 어느 하나라도 벽이면 벽임
    # 모두 공백은 공백임
    secretMap = []
    for i in range(n):
        check = bin(arr1[i] | arr2[i])[2:].zfill(n)
        check = check.replace('1', '#')
        check = check.replace('0', ' ')
        secretMap.append(check)
            
   
    return secretMap
```

## zfill(n), ljust, rjust, center

n 자리수의 껍데기에 맞추어서 숫자 앞에 0을 붙여 넣는다. <br>
ljust, rjust, center (자릿수, 넣을 문자 (default = 공백)) <br>

```py
print('123'.zfill(5)) # 00123

print('123'.ljust(5)) # 123
print('123'.rjust(5)) #   123
print('123'.center(5)) # 123 

print('123'.ljust(5,'*')) # 123**
print('123'.rjust(5,'*')) # **123
print('123'.center(5,'*')) # *123*

```

