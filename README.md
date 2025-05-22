# dify-try
一个dify项目

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




