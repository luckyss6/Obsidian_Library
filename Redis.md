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

curl -sfL https://rancher-mirror.rancher.cn/k3s/k3s-install.sh | INSTALL_K3S_MIRROR=cn K3S_URL=https://10.0.20.10:6443 K3S_TOKEN=K107f0732679939b4555da00ba17bd60b445d0765caf3c0fc5ccab47176bd7e73ba::server:6714af2177cd1dad59824db15b9eb8fc sh -s - --docker

kubectl label node salve kubernetes.io/role=worker