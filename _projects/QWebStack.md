---
title: QWebStack
collection: projects
excerpt: 'A Django version of the WebStack navigation site, including management, database, using SimpleUI theme in the management.'
date: 2021-11-18
venue: 'Github'
projecturl: 'https://github.com/Quanfita/QWebStack'
---

A Django version of the WebStack navigation site, including management, database, using SimpleUI theme in the management.

[WebStack](https://github.com/WebStackPage/WebStackPage.github.io)

## 运行环境

- Python3.6
- Django2.x
- sqlite3/MySQL
- SimpleUI

## 安装运行

```shell
git clone https://github.com/Quanfita/QWebStack.git  
cd QWebStack  
pip install -r requirements.txt  
python manage.py runserver
```

默认使用sqlite，已有数据，如需要导出到MySQL或者其他数据库，使用以下命令导出

```shell
python manage.py dumpdata > data.json
```

然后，修改QWebStack/settings.py，将DATABASES修改为MySQL的相关配置，然后使用以下命令

```shell
python manage.py makemigrations
python manage.py migrate
python manage.py loaddata data.json
```

最后运行即可

```shell
python manage.py runserver
```

## 致谢
感谢 [Viggo](http://viggoz.com/) 的前端设计和数据提供。