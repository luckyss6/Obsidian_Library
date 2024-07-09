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
	

curl -sfL https://rancher-mirror.rancher.cn/k3s/k3s-install.sh | INSTALL_K3S_MIRROR=cn INSTALL_K3S_EXEC="--tls-san 139.199.192.95" sh -s - --docker

curl -sfL https://rancher-mirror.rancher.cn/k3s/k3s-install.sh | INSTALL_K3S_MIRROR=cn K3S_URL=https://10.0.20.10:6443 K3S_TOKEN=K1032c61c9c4b49538154ff93fd618a04eaefca3ceb0e488acd1d5f16164eea9781::server:5548c06481292bf42bfc45cd9d1e1cd6 sh -s - --docker

kubectl label node salve kubernetes.io/role=worker