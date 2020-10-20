---
title: "선택 정렬"
excerpt: ""
date: 2020_10_20
categories: algorithm
tags:
last_modified_at: 2020-10-20 23:09:20
toc: true
toc_sticky: true
---

## [문제08 선택정렬](https://thebook.io/006935/part03/ch08/)

### 정렬의 종류

    1. 선택정렬
    2. 삽입정렬
    3. 병합정렬
    4. 퀵정렬
    5. 거품정렬

### 선택정렬

- 대상중에서 최소값을 선택하여 순차적으로 줄세우는 알고리즘
- 시간복잡도는 O(n^2^)

```python
def find_min_idx(a):
    min_idx = 0
    for i in range(1, len(a)):
        if a[i] < a[min_idx]:
            min_idx = i
    return min_idx


def sel_sort(a):
    result = []
    while a:
        result.append(a.pop(find_min_idx(a)))
        print(result)
    return result

def normal_sel_sort(a):
    n = len(a):
    for i in range(0, n-1):
        min_idx = 1
        for j in range(i+1, n):
            if a[j] < a[min_idx]:
                min_idx=j
        a[i], a[min_idx] = a[min_idx], a[i]


my_list = [13, 22, 3, 5, 11, 2, 5, 7, 22, 33]
print(find_min_idx(my_list))
print(sel_sort(my_list))
```
