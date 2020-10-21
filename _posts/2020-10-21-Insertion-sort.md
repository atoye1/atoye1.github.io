---
title: "삽입정렬"
excerpt: "삽입정렬 알고리즘을 알아본다."
date: 2020_10_21
categories: algorithm
tags: algorihtm
last_modified_at: 2020-10-21 05:44:51
toc: true
toc_sticky: true
---

## 쉽게 설명한 삽입정렬 알고리즘
```python
def find_ins_idx(r,v):
    for i in range(0, len(r)):
        if r[i] > v:
            return i
    return len(r)

def ins_sort(a):
    result = []
    while a:
        value = a.pop(0)
        ins_idx = find_ins_idx(result, value)
        result.insert(ins_idx, value)
    return result
```

- 일반적인 삽입정렬 알고리즘은 다음과 같다.
    - 손안의 카드를 정렬하는 방법과 유사하다
    - 자료 배열의 모든 요소를 앞에서부터 차례대로 이미 정렬된 배열 부분과 비교하여, 자신의 위치를 찾아 삽입함으로써 정렬을 완성하는 알고리즘
    - 매 순서마다 해당 원소를 삽입할 수 있는 위치를 찾아 해당 위치에 넣는다

- 삽입정렬 알고리즘의 구체적인 개념
    - 처음 key값은 두 번째 자료부터 설정한다.
    - 삽입할 위치를 찾았으면, 모든 자료를 뒤로 한칸씩 이동시켜야한다.

### 파이썬으로 표현한 선택정렬

```python
def normal_selection_sort(li):
    n = len(li)
    for i in range(1, n): # 2번째부터 마지막 값까지
        key = li[i] #2번째 값을 키로 지정한다.
        j = i-1 #i의 왼쪽 공간을  j 로 정한다.
        while j >= 0 and li[j] > key: #왼쪽 공간이 존재하고, 왼쪽의 값이 키값보다 크면
            li[j+1] = li[j] # 왼쪽 값을 키 자리에 복사함으로서 키값을 리스트에서 없앤다.
            j -= 1 # 왼쪽으로 한칸 더 진행해서 반복한다.
        li[j+1] = key # 더 이상 키값보다 큰 값이 없을때의 인덱스는 j+1이므로 키값을 해당 인덱스에 할당한다.

my_list = [5, 3, 2, 9, 1, 31, 22]
normal_selection_sort(my_list)
print(my_list)
```