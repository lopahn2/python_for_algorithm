# 모듈 정리 (사용하는 것만)

## collection

#### Counter
보유한 주식이 다음과 같을 때, 종목별로 합산해 나타내고 싶다고 하자. <br>
```python
portfolio = [
    ('GOOG', 100, 490.1),
    ('IBM', 50, 91.1),
    ('CAT', 150, 83.44),
    ('IBM', 100, 45.23),
    ('GOOG', 75, 572.45),
    ('AA', 50, 23.15)
]
# 주식명 / 주식 수 / 가격
```
위 리스트에  `IBM`과  `GOOG`가 두 개씩 있다. 종목별로 합산해 보자. <br>

```python
from collections import Counter

total_shares = Counter()

for name, shares, price in portfolio:
    total_shares[name] += shares

total_shares['IBM']     # 150
```

#### 일대다(One-Many) 매핑 (defaultdict)

하나의 키를 여러 개의 값에 매핑하려고 한다. <br>
```python
portfolio = [
    ('GOOG', 100, 490.1),
    ('IBM', 50, 91.1),
    ('CAT', 150, 83.44),
    ('IBM', 100, 45.23),
    ('GOOG', 75, 572.45),
    ('AA', 50, 23.15)
]
```

앞의 예와 같이,  `IBM`을 키로 삼으면 두 개의 튜플이 있다. <br>


```python
from collections import defaultdict

holdings = defaultdict(list) # portfolio가 아니라 list라 쓰는게 맞다.

for name, shares, price in portfolio:
    holdings[name].append((shares, price))
    
holdings['IBM'] # [ (50, 91.1), (100, 45.23) ]

```

**`defaultdict`** 을 사용하면 키에 액세스할 때마다 기본값을 얻는다. <br>


<br>
<br>
<br>

## Math

```python-repl
>>> import math
```

#### 올림 - ceil
```python-repl
>>> math.ceil(3.14) #4
```

#### 내림 - floor

```python-repl
>>> math.floor(3.78)    #3

>>> math.floor(-3.14)   #-4
>>> math.trunc(-3.14)   #-3
```
trunc()함수는 0으로 향하지만 floor()함수는 무조건 아래로만 향한다. <br>

#### 부호 취하기 - copysign

```python-repl
>>> math.copysign(3.14, -3) #-3.14

# 두 번째 인자의 부호만 취해 첫 번째 인자에 적용
```


#### 절댓값 - fabs

```python-repl
>>> math.fabs(-3.14)    #3.14
```

#### 팩토리얼 - factorial

```python-repl
>>> math.factorial(5)   #120
```

### 최대 공약수 반환 - gcd
```python-repl
>>> math.gcd(6, 8)  #2
```

TIP : 최소 공배수는 a * b / gcd <br>

#### 정수부 소수부 구분 - modf

```python-repl
>>> math.modf(3.14) #(0.14000000000000012, 3.0)
```

math.modf() 함수는 입력값을 정수와 소수 부분으로 분리해 반환한다.   <br>
modf()함수는 부동소수점의 값을 그대로 반환한다.

