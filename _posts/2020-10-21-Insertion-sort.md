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