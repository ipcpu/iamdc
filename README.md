# iamdc
运维自动化平台(iamdc)

暂时未编写此文件 ， 可以查看 http://www.huangdc.com

##追加说明 

Python版本2.7.5

建议使用virtualenv

##安装方法

pip install -r requirements.txt

修改iamdc/settings.py 中的数据库配置

初始化数据库
python manage.py makemigrations dashboard
python manage.py migrate

插入测试数据，进入数据库执行
```
INSERT INTO `dashboard_department` VALUES (1,'sa','sa','2016-12-23 08:53:42','2016-12-23 08:53:42');
INSERT INTO `dashboard_users` VALUES (1,'admin','admin','123456','admin@huangdc.com',2,0,'2016-12-23 08:55:49','2016-12-23 08:55:49',1,1),(2,'user01','user01','123456','user01@huangdc.com',1,2,'2016-12-23 09:07:54','2016-12-23 09:07:54',1,1);
```
用户名admin密码123456

##启动程序
python manage.py runserver 0.0.0.0:9998
