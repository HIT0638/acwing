# Acwing docker配置课程的note

1. 进入云服务器
2. 下载配置 docker 环境 ` 参考 docker官方文档 `
3. 将 ACTerminal 的 docker_lesson 镜像传到云服务器 `scp ... server1:`
4. 将 rar 下载到云服务器目录 `docker load -i ...`
5. 在该镜像下创建容器 端口为20000:22 `docker run -p 20000:22 --name my_docker_server -itd docker_lesson:1.0` 
6. 在云服务器端将容器用户添加到 docker 用户组 `sudo usermod -aG $USER`
7. 在容器根目录创建工作用户 `adduser ...`
8. 给根目录 root 下载sudo `apt-get install sudo`
9. 出去给容器配置 `ssh-config` 、 `免密`
10 进入容器 root 用户下下载 tmux `sudo apt-get install tmux`
11 将祖传代码上传到容器 `scp .bashrc .vimrc .tmux.conf server1_docker:` 