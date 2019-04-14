Python3.54  Django2.1
account_py3_dj21
外键使用， 不用特别处理，模板就能渲染。


一、功能：
高域传媒

二、相关技术
（一）时间格式
1、设置环境（中国时区）：settings.py
LANGUAGE_CODE = 'zh-Hans'
TIME_ZONE = 'Asia/Shanghai'
2、models.py
date = models.DateTimeField(default=datetime.datetime.now, null=True, blank=True)
3、views.py
o = Order()
o.date = datetime.datetime.now()-datetime.timedelta(days=random.randint(1, 500))
o.save()
4、前端 html输出格式：
{{ i.date }} 2018年11月15日 10:26
{{ i.date | date:"Y-m-d H:i:s" }}   2018-11-15 10:26:44


