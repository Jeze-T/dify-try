# dify-try
一个dify项目

学习入门参考：https://www.bilibili.com/video/BV1TD421n7Zd/?vd_source=75754cddd52ade3e8753104493cc5741&spm_id_from=333.788.videopod.sections

运行结果：

![image](https://github.com/user-attachments/assets/4164c654-002e-47a9-9955-139d56c1eed8)


dify安装参考：https://zhuanlan.zhihu.com/p/1897651300860158702

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

