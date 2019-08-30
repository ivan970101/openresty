# openresty
some openresty examples

# 项目介绍
流量转发：流量分为3种。
        请求A需要根据不同的路径转发到不同的实例 
        请求B需要根据不同的参数转发到不同的实例
        请求C需要按权重转发
# 测试
根据test.conf中的端口相应的起服务 这里用的是python的flask 起了两个不同的端口看效果
nginx -c home/work/develop/test/conf/test.conf 路径请根据需要更换

# 调试时 nginx 常用命令
nginx -c xxx.conf 启动并指定读取的配置文件 建议配置文件不要用安装路径的配置文件
nginx -s reload 如果修改配置文件需要重新加载
nginx -s stop 关闭nginx 或者 ps-ef|grep nginx kill掉相应的进程号
nginx -s quit 等待旧连接释放后自动关闭
