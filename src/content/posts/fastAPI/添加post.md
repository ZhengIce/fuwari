---
title: 添加 POST 路由
published: 2025-12-08
tags: [fastapi, python]
category: fastapi
draft: false
---

# 处理 POST 请求
```python
from fastapi import FastAPI
from pydantic import BaseModel
from typing import List

app = FastAPI()

class TodoCreate(BaseModel):
    title: str

# 模拟数据库（实际用 SQLite 或 PostgreSQL）
todos = []

@app.get("/todos", response_model=List[TodoCreate])
def get_todos():
    return todos

@app.post("/todos")
def add_todo(todo: TodoCreate):
    todos.append(todo)
    return {"message": "Todo added", "todo": todo}

```
> response_model 告诉 FastAPI：这个接口返回的数据，必须是一个 TodoCreate 对象的列表，并且 FastAPI 会自动把数据“转换 + 过滤”成符合这个结构的 JSON。