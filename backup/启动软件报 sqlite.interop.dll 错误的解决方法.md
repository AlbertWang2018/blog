一个调试软件，一启动就报找不到  sqlite.interop.dll ，但这软件在我电脑上正常的，我判断是win10或11系统环境问题，最大可能是缺少vc运行库。以前我是手动下载安装的，麻烦，目前我找到的最方便的方法是一条命令： 
`winget install vcredist `
![image](https://github.com/AlbertWang2018/blog/assets/36392874/5163082c-ea8f-4347-9d8a-2e4f0bde18ee)

2分钟搞定，省事。
![error](https://github.com/AlbertWang2018/blog/assets/36392874/b2886cf2-f84b-498a-afa4-1f246a349a07)
