# 함수 정리

## 진수 변환

```py
a = 200

# 접두어 포함
b = '{:#b}'.format(a)
print(f"2진수 : {b}")

c = '{:#o}'.format(a)
print(f"8진수 : {c}")

d = '{:#x}'.format(a)
print(f"16진수 : {d}")

b = format(a, '#b')
print(f"2진수 : {b}")

c = format(a, '#o')
print(f"8진수 : {c}")

d = format(a, '#x')
print(f"16진수 : {d}")

[결과]
2진수 : 0b11001000
8진수 : 0o310
16진수 : 0xc8
2진수 : 0b11001000
8진수 : 0o310
16진수 : 0xc8

# 접두어 제외
b = format(a, 'b')
print(f"2진수 : {b}")

c = format(a, 'o')
print(f"8진수 : {c}")

d = format(a, 'x')
print(f"16진수 : {d}")

[결과]
2진수 : 11001000
8진수 : 310
16진수 : c8
```

