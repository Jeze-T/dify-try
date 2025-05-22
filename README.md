# dify-try
一个dify项目

学习入门参考：https://www.bilibili.com/video/BV1TD421n7Zd/?vd_source=75754cddd52ade3e8753104493cc5741&spm_id_from=333.788.videopod.sections

运行结果：

![image](https://github.com/user-attachments/assets/4164c654-002e-47a9-9955-139d56c1eed8)

官网：
https://cloud.dify.ai/

一开始想用Github工具，通过传入搜索关键词来搜索相关仓库，再获取仓库的README内容，然后让LLM生成一个JSON格式的内容，包括仓库名，仓库README摘要，仓库链接，最后通过邮件发送。

但是Github工具好像有点问题，传入不了输入。不止这个工具，一些其他工具也有这样的问题。

后续优化：

Windows 计划任务每天准时运行一个非常简单的 PowerShell 脚本，该脚本仅负责安全地触发 Dify 上的 Webhook URL。随后，Dify 工作流被激活，自动执行日期和天气获取、生成穿衣建议，并通过集成的 163 邮件插件将结果发送到你的指定邮箱。核心的邮件发送逻辑和凭据管理都在 Dify 平台内部完成。

参考https://blog.csdn.net/xiaonie1986/article/details/147464255

----------------------------------------------------------------------

本地dify安装参考：https://zhuanlan.zhihu.com/p/1897651300860158702

（事实上不需要本地安装）

下载dify源码 https://github.com/langgenius/dify

然后 进入到源代码中的 docker 目录下

cd dify/docker

cp .env.example .env

docker compose up -d

不成功需要修改docker镜像源

sudo nano /etc/docker/daemon.json

{
    "registry-mirrors": [
    
        "https://hub.uuuadc.top",
        
        "https://docker.anyhub.us.kg",
        
        "https://dockerhub.jobcher.com",
        
        "https://dockerhub.icu",
        
        "https://docker.ckyl.me",
        
        "https://docker.awsl9527.cn",
        
        "https://docker.m.daocloud.io",
        
        "https://docker.nju.edu.cn",
        
        "https://dockerproxy.com"

    ]
    
}

sudo systemctl daemon-reload

sudo systemctl restart docker


确认是否安装成功

在终端中输入：docker ps

在确认DOCKER已经开起的情况下，设置DIFY，在浏览器输入127.0.0.1/install
设置完成后，可以进入界面

