# cmp_to_key

```python
from functools import cmp_to_key

def compare(x, y):
    if x+y > y+x:
    	return -1
    elif x+y == y+x:
    	return 0
    else:
    	return 1
      
sorted(list, key = cmp_to_key(compare)
```

return 음수 : 먼저 들어온 요소가 앞으로 정렬됨 <br>
return 0 : 바뀌지 않음 <br>
return 양수 : 나중에 들어온 요소가 앞으로 정렬됨(먼저들어온 요소보다 앞에 배치됨) <br>

<br>
즉, if 문을 통해 정렬 조건을 선택하고, 그 케이스에 뒤에 있는 원소가 앞으로 갈지, 뒤로 갈지, 그 위치를 고수할지 선택하면 된다!!
