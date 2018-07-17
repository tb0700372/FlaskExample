# 说明

## 准备工作

```bash
# 进入项目主目录
mkdir app               # 创建APP目录
mkdir app/static        # 创建静态资源目录
mkdir app/templates     # 创建模板目录
mkdir tmp               # 创建缓存目录
```

## APP初始化

[./app/\_\_init\_\_.py](./app/\_\_init\_\_.py)

```python
from flask import Flask

app = Flask(__name__)
from app import views
```

## APP视图

[./app/views.py](./app/views.py)

```python
from app import app

@app.route('/')
@app.route('/index')
def index():
    return "Hello, World!"
```

## 服务文件

[./run.py](./run.py)

```python
#!flask/bin/python
from app import app
app.run(debug = True)
```

## 运行

```bash
python run.py
```
