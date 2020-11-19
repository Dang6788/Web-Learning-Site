本文件夹中的代码为部署在阿里云服务器上的最终版本的网站代码，代码中的参数（例如IP、端口、MySQL数据库等）、路径以阿里云服务器相应的配置参数和路径为准。若需要在本地主机上运行调试代码，应当按如下步骤进行操作：



1. 按需求安装相应的python包，例如flask, flask-script, sqlalchemy等，推荐使用python2.7环境；

2. 在本地安装MySQL数据库，推荐使用MySQL 5.7版本，之后在config.py对MySQL密码、数据库名称等参数进行相应修改；

3. 对app.py中上传和下载文件的路径进行修改；

4. 对app.py的主函数入口参数进行修改，可以直接改为如下形式：

   if __name__ ='__main__':

   ​	app.run(debug=True)

5. 在manage.py所在文件目录下，运行如下命令，进行数据库的迁移：

   python manage.py db init

   python manage.py db migrate

   python manage.py db upgrade

6. 迁移成功后即可在本地进行测试运行。





