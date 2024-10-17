# k8s_install 项目使用说明 

## 项目介绍： 
本项目用于离线安装k8s 1.23.17版本，适用于业务场景中纯内网安装

## 项目目录结构： 
```
offline_install_k8s_1.23.17
├── ansible.cfg
├── base
│   ├── create_repo
│   ├── get_arch.sh
│   ├── offline_install_ansible
│   ├── offline_install_docker
│   ├── push_image
│   ├── show_help.sh
│   ├── ssh_speed_up.sh
│   └── welcome.sh
├── hosts
├── local_repo
│   ├── image
│   └── yum
├── roles
│   ├── base
│   ├── chrony
│   ├── install_k8s
│   ├── k8s_init
│   ├── k8s_join_node
│   ├── kernel_module
│   ├── offline_install_docker
│   ├── ping
│   └── push_image
├── start.sh
└── use_ansible_roles
    ├── base
    ├── install_k8s
    ├── ping
    └── push_image
```

## 使用说明：

### 帮助介绍
```
  ____              ___            
 |  _ \  _____   __/ _ \ _ __  ___ 
 | | | |/ _ \ \ / / | | | '_ \/ __|
 | |_| |  __/\ V /| |_| | |_) \__ \
 |____/ \___| \_/  \___/| .__/|___/
                        |_|        

使用方法: ./start.sh [选项]

选项:
	init             初始化服务
	install_k8s      安装k8s
	list             列出所有选项
	add_image        导入镜像到registry(仅限于新添加镜像导入)
	--help           显示此帮助信息

EXAMPLE: 
	./start init 
	./start install_k8s

```

### 使用步骤：
```
git clone https://github.com/azheno/offline_install_k8s
cd offline_install_k8s_1.23.17/
./start init
./start install_k8s 
```
