#  安装Sublime text 3#
    从Sublime text3 官网下载安装包 
    http://www.sublimetext.com/
# 安装nodejs #
    下载nodejs安装包 https://nodejs.org/
# 安装npm #
    https://www.npmjs.com/
# 安装nodejs在sublime插件 #
  
>  git clone https://github.com/tanepiper/SublimeText-Nodejs "D:\Software\Sublime Text 3\Packages\Nodejs" 

   后面路径是本地Sublime Text 3 （Preferences–>浏览程序包Browse Packages所在的文件夹）


  然后打开刚才下载到本地的地址下面的 Nodejs.sublime-build 文件 修改两个地方

1. 编码
2. 启动NodeJS进程命令

配置完文件内容
{
  "cmd": ["node", "$file"],
  "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
  "selector": "source.js",
  "shell":true,
  "encoding": "cp936",
  "windows":
    {
    	"cmd": ["taskkill","/F", "/IM", "node.exe","&","node", "$file"]
    },
  "linux":
    {
        "cmd": ["killall node; node", "$file"]
    },
    "osx":
    {
	"cmd": ["killall node; node $file"]
    }
}



然后重启sublime text


# 写NodeJs程序测试 #



 




   
