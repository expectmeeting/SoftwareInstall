# cmake安装

cmake是一款跨平台的编译工具，可以生成makefile或者project。

## 自动安装

~~~
$ yum install cmake
$ sudo apt-get install cmake
~~~

上面任意一条命令都可自动安装cmake，安装成功后，可使用下面的命令查看版本。

~~~
$ cmake --version
~~~

## 手动安装

首先，查看自己的系统是多少位的。

~~~
$ getconf LONG_BIT
~~~

然后，上[官网][https://cmake.org/download]下载对应的压缩包。

![fig 1](C:\git_repository\SoftwareInstall\cmake\fig1.png)

~~~
$ wget https://cmake.org/download/cmake-3.13.4-Linux-x86_64.tar.gz
~~~

将下载好的包复制到指定路径（如root/cmake），然后进行解压

~~~
$ tar zxvf cmake-3.13.4-Linux-x86_64.tar.gz 
~~~

编辑.bash_profile，找到export PATH=这些行，在这些行的后面添加：/root/cmake/bin，从而设置环境变量。

~~~
  1 # .bash_profile
  2
  3 # Get the aliases and functions
  4 if [ -f ~/.bashrc ]; then
  5     . ~/.bashrc
  6 fi
  7
  8 # User specific environment and startup programs
  9
 10 PATH=$PATH:$HOME/bin:/root/cmake/bin
 11
 12 export PATH
~~~

保存退出后，查看版本，判断是否安装成功。