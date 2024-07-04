1. 持久化
	>RDB
	>  定时将内存里头的数据保存到硬盘当中,dump.rdb
	>AOF
	>	每一次写操作,都会追加到aof文件末尾
	>混合持久
	

2. 过期删除
	>- 定时抽取删除
	>- 惰性删除


3. 淘汰策略
	> - 不进行数据淘汰的策略
	> - 进行数据淘汰的策略
	> - 对于有过期时间的数据和全局数据

4. 缓存问题
	> 雪崩,击穿,穿透
		> 雪崩: 大量key同时过期
		> 击穿: 热点key过期
		> 穿透: 访问不存在的数据
	
	> 数据库缓存一致性
	> 旁路缓存模式
	
LUCKY123!@#HELO

grpcurl -d '{"id": 1234, "tags": ["foo","bar"]}' \
    localhost:50051 my.custom.server.Service/Method

docker run --name test-api-gateway \
 -v /example/apisix_conf/:/usr/local/apisix/conf/\
 -v /example/apisix_log:/usr/local/apisix/logs  \
 -p 9080:9080 \
 -p 9091:9091  \
 -p 9443:9443 \
 -d apache/apisix