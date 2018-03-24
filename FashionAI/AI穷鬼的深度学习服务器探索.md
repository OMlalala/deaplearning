# AI穷鬼的深度学习服务器探索
- - - -
## 背景
- 深度学习需要很高的GPU算力
	- 自己攒一台基础配置的深度学习主机需要1.5万左右
	- 租服务器
	
- - - -
## 深度学习服务器选择
- AWS
- crestle
- paperspace
- - - -

## GPU性价比
以算力相同的GPU做比较
- AWS
	- K80,0.9$/h
- crestle
	- K80, 0.59$/h
- paperspace
	- P4000,0.4$/h
- - - -
## 其他费用
- 费用动态切换
	- crestle 可以开机后在GPU和CPU之间一键切换，cpu费用，0.059¥/h
	- paperspace, 只要一开机，就一直按GPU费用收费
- 硬盘
	- crestle, 0.014$/GB/Day
	- paperspace,50GB, 5$ /Month,100GB,6$/Month
	-  当硬盘容量超过12GB时，paperspace比crestle更便宜
- 公网IP
	- crestle无
	- paperspace,1$/Month
- - - -
## 用户体验
- 上手速度
	- crestle无需任何配置，直接jupyter notebook上手，及其简单
	- paperspace，需要配置jupyter notebook到本地的映射
- CLI流畅度
	- 由于服务器都在国外，CLI都会有写卡顿
- jupyter notebook加载速度
	- paperspace有时本地加载一个jupyter notebook需要2到3分钟，但是加载完毕后，运行流畅
- 和本地的数据交互速度
	- 两者都可以用scp，速度在500K-1M左右
	- paperspace可以安装网盘，比如Dropbox，实现数据异步交互
		
- - - -
## 如何选择
- GPU算力
	- crestle 只有k80一种GPU
	- paperspace有p4000,P5000,P6000更高算力的GPU
		- P6000 相当于K80的三倍，0.9$/h
- 费用动态切换
	- 开机后，crestle支持按照CPU费用
-  灵活性
	- papersapce更加灵活，可以安装提升效率的软件