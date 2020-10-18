---
title: "파이썬 코드조각"
excerpt: "카테고리와 태그 연습을 위해 작성한 포스트"
date: 2020_10_19 
categories: python
tags: python snippet
last_modified_at:
---

## 파이썬 코드조각 입니다.
```python
import bs4
import requests

res = requests.get("https://torrent.movie")
soup = bs4.BeautifulSoup(res.content, "html.parser")
```
