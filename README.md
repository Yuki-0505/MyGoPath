# `VSCode`中配置Go

## 1. 下载

> <https://golang.google.cn/>

## 2. `Linux`

### 2.1. 解压安装到`/usr/local/`目录下

```bash 
sudo tar -xzvf go1.13.4.linux-amd64.tar.gz -C /usr/local/
```

### 2.2. 配置环境变量

#### 2.2.1. 打开配置文件

```bash
sudo vim /etc/profile
```

#### 2.2.2. 在文件最后添加环境变量

```bash
# GOROOT
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
# GOPATH
export GOPATH=/usr/local/gopath
export PATH=$PATH:$GOPATH
# GOPROXY
export GOPROXY=https://goproxy.cn
export PATH=$PATH:$GOPROXY
```

#### 2.2.3. 保存退出

> `Esc` `:wq` `Enter`

## 3. `Windows`

### 3.1. 双击安装程序安装

### 3.2. 配置环境变量

> 右键此电脑 =》 属性 =》 高级系统设置 =》 环境变量

```bash
GOROOT
D:\Go
GOPATH
D:\GoPath
GOPROXY
https://goproxy.cn
PATH
%GOROOT%\bin
```

## 4. `VSCode`中配置插件

> 在`VSCode`打开`gopath`目录，`Ctrl` `Shift` `P`打开命令面板，输入`go:install/update tools`并选中，勾选所有选项，确定，等待安装完成