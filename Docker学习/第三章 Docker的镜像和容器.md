# 创建一个base Image
```javascript
创建一个base image
vim Dockerfile
==>
    FROM scratch
    ADD hell /
    CMD ["/hello"]
wq 保存退出

docker build -t endlessday3/hello-world .   # 从当前目录去找Dockerfile创建一个tag为endlessday3/hello-world的镜像
==> 过程中会产生对应的中间层镜像

docker image ls 查看到有endlessday3/hello-world的镜像存在了

docker histort *IMAGE ID*   # 通过此命令可以查看image的分层

# 我们可以用这个image执行一个container
docker run endlessday3/hello-world => hello world!
```
