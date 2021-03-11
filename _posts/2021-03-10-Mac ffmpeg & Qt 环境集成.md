

title:  "Dart 语法 blog"
date:   2021-03-10 11:38:23
categories: [ilife-x]

tags: [ilife-x]

#### ##brew 配置

参考连接 ：https://cnblogs.com/mjios/p/14497925.html#toc_title_9

## 官方

> [Homebrew](https://brew.sh/)是Mac上非常优秀的软件包管理工具。

### 前提

Mac安装Homebrew的[前提条件](https://docs.brew.sh/Installation)：

- 64bit Intel CPU或Apple Silicon CPU（M1）
- macOS Mojave（10.14）或更高版本
- 安装Xcode命令行工具（Command Line Tools for Xcode）
  - 可以通过命令行*xcode-select --install*安装
- shell（比如bash或zsh）

### 安装

打开终端，输入以下命令：

```sh
复制代码
SH/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 其他安装方法

由于国内的网络环境等问题，使用官方的安装方法可能无法安装成功。可以尝试使用其他更适合国内网络环境的安装方法，参考地址：https://brew.idayer.com/。

### 安装homebrew-core

```sh
复制代码
SH/bin/bash -c "$(curl -fsSL https://cdn.jsdelivr.net/gh/ineo6/homebrew-install/install.sh)"
```

### 安装homebrew-cask

```sh
cd "$(brew --repo)/Library/Taps/homebrew/"
 
git clone https://mirrors.ustc.edu.cn/homebrew-cask.git
```

## 源

为了加速以后使用Homebrew安装其他软件的过程，建议设置软件源为国内源。

### 查看源

```sh
cd "$(brew --repo)" && git remote -v
 
cd "$(brew --repo homebrew/core)" && git remote -v
 
cd "$(brew --repo homebrew/cask)" && git remote -v
```

### 设置源

设置为中科大的源

```sh
git -C "$(brew --repo)" remote set-url origin https://mirrors.ustc.edu.cn/brew.git
 
git -C "$(brew --repo homebrew/core)" remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
 
git -C "$(brew --repo homebrew/cask)" remote set-url origin https://mirrors.ustc.edu.cn/homebrew-cask.git
 
brew update
```

### 设置bottles镜像

从macOS Catalina(10.15.x) 版开始，Mac使用zsh作为默认shell，使用的配置文件：.zprofile

```sh
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.zprofile
 
source ~/.zprofile
```

如果是以前的macOS版本，Mac使用bash作为默认shell，使用的配置文件：.bash_profile

```sh
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile
 
source ~/.bash_profile
```

### 重置为官方源

### 重置为官方源

可以通过以下命令还原回官方源。

```sh
git -C "$(brew --repo)" remote set-url origin https://github.com/Homebrew/brew.git
 
git -C "$(brew --repo homebrew/core)" remote set-url origin https://github.com/Homebrew/homebrew-core.git
 
git -C "$(brew --repo homebrew/cask)" remote set-url origin https://github.com/Homebrew/homebrew-cask.git
 
# zsh 注释掉 HOMEBREW_BOTTLE_DOMAIN 配置
vi ~/.zprofile
# export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles
source ~/.zprofile
 
# bash 注释掉 HOMEBREW_BOTTLE_DOMAIN 配置
vi ~/.bash_profile
# export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles
source ~/.bash_profile
 
brew update
```

## 卸载

```sh
复制代码
SH/usr/bin/ruby -e "$(curl -fsSL https://cdn.jsdelivr.net/gh/ineo6/homebrew-install/uninstall)"
```

分类: [工具](https://www.cnblogs.com/mjios/category/1943066.html)



## 截图

FFmpeg 安装完成后截图

![截屏2021-03-10 下午11.45.03](/Users/wangxiao/ilife-x/images/ffmpeg_blog/截屏2021-03-10 下午11.45.03.png)



！如果已经安装了一遍，二次安装的时候用 'brew reinstall ffmpeg' 命令，会有提示

![截屏2021-03-10 下午11.45.55](/Users/wangxiao/Library/Application Support/typora-user-images/截屏2021-03-10 下午11.45.55.png)



安装 qt

![截屏2021-03-10 下午11.48.01](/Users/wangxiao/Desktop/截屏2021-03-10 下午11.48.01.png)

成功后 安装 qt-creator,( brew install --cask qt-creator 命令),表示安装大型应用，

![截屏2021-03-10 下午11.49.24](/Users/wangxiao/Library/Application Support/typora-user-images/截屏2021-03-10 下午11.49.24.png)



如果不知道是否需要添加--cask，可以到brew官网查询

[homebrew](https://brew.sh/)

![截屏2021-03-10 下午11.52.35](/Users/wangxiao/Library/Application Support/typora-user-images/截屏2021-03-10 下午11.52.35.png)



![截屏2021-03-10 下午11.53.11](/Users/wangxiao/Library/Application Support/typora-user-images/截屏2021-03-10 下午11.53.11.png)



安装完成后可以在应用广场看到

![截屏2021-03-10 下午11.54.36](/Users/wangxiao/Library/Application Support/typora-user-images/截屏2021-03-10 下午11.54.36.png)



## 项目配置





![1](/Users/wangxiao/Desktop/1.png)

![2](/Users/wangxiao/Desktop/2.png)



修改默认

![截屏2021-03-10 下午10.38.24](/Users/wangxiao/Desktop/截屏2021-03-10 下午10.38.24.png)



![截屏2021-03-10 下午10.39.19](/Users/wangxiao/Desktop/截屏2021-03-10 下午10.39.19.png)





![image-20210310235737245](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210310235737245.png)



![image-20210310235757418](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210310235757418.png)



![image-20210310235903990](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210310235903990.png)



![image-20210310235936856](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210310235936856.png)





![image-20210311000007422](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000007422.png)





![image-20210311000022543](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000022543.png)



![image-20210311000106648](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000106648.png)



![image-20210311000152110](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000152110.png)



![image-20210311000213322](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000213322.png)



至此创建完成

### 问题

如果默认的不是Desktop-64位，可以到偏好设置中修改，刚刚安装的默认的应该是最后一个

![image-20210311000416632](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000416632.png)



### FFmpeg 配置

![image-20210311000603064](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000603064.png)



仔细看这些链接的库，就是FFmpeg文件安装的里面的库，注意名称的变化(libavcodec --> -lavcodec)

![image-20210311000750071](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311000750071.png)



![image-20210311001121322](/Users/wangxiao/Library/Application Support/typora-user-images/image-20210311001121322.png)

