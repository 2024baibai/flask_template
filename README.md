# Flask蓝图模板

**为什么建一个flask_template项目？**

因为要用flask搭建一个网站总是一个痛苦的过程，不像Django，可以通过命令一键搭建一个*简易网站*出来

所以想要自己建一个模板出来，每次用flask搭建网站时，只需要git clone下来这个项目，然后再通过修改本项目的代码，进行web开发。

**Python Web开发者**可通过clone这个项目，快速搭建一个flask起手架，无需一个文件一个文件去搭建一个flask网站框架。


**如何使用?**

```
git clone https://github.com/abbeyokgo/flask_template.git #下载源码
cd flask_template #切换到目录下
pip install -r requirements.txt
python manage.py db init #初始化数据库
python manage.py db migrate #迁移
python manage.py db upgrade #升级
python manage.py runserver #运行
```

运行网站之后，提示
```
[root@centos flask_template]# python manage.py runserver
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 128-717-467
```

然后浏览器打开：`127.0.0.1:5000`即可

![](https://ws1.sinaimg.cn/large/0074MymAgy1fz8a6oftzyj30y40a074j.jpg)



**文件树**
```
flask_template/
├── app #主目录
│   ├── email.py #发送邮件的脚本
│   ├── __init__.py
│   ├── main #主视图文件夹
│   │   ├── errors.py
│   │   ├── forms.py
│   │   ├── __init__.py
│   │   └── views.py #主视图脚本
│   ├── models.py #全局models脚本
│   ├── static #静态文件目录
│   │   └── favicon.ico
│   └── templates #HTML模板目录（jinja2语法）
│       ├── 404.html
│       ├── 500.html
│       ├── base.html
│       ├── index.html
│       └── mail
│           ├── new_user.html
│           └── new_user.txt
├── config.py #配置文件
├── LICENSE
├── manage.py #运行脚本
├── README.md
├── requirements.txt #依赖包
└── tests #单元测试目录
    ├── __init__.py
    └── test_basics.py
```
