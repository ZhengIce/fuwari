---
title: FastAPI 快速入门
published: 2025-12-08
tags: [fastapi, python]
category: fastapi
draft: false
---

# 安装
```bash
pip install fastapi uvicorn[standard]
```
> fastapi 是一个基于 Python 的现代 Web 框架，用于构建快速、高效的 API。

> uvicorn 是一个 ASGI 服务器，用于运行 fastapi 应用。

> standard 扩展提供了额外的功能，如自动重新加载、调试模式等。

# 第一个应用
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}
```
## 运行应用
```bash
uvicorn main:app --reload
```
> 访问 `http://127.0.0.1:8000/` 即可看到 "Hello, World!"

> 访问 `http://127.0.0.1:8000/docs` 即可查看 API 文档。