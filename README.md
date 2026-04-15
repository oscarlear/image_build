# image_build
build image by github action

# 1. 创建一个临时容器 (不会启动)
docker create --name temp-container my-image:latest

# 2. 从临时容器中拷贝文件到当前目录
# 语法: docker cp <容器名>:<容器内路径> <本地路径>
docker cp temp-container:/packages/ol8_offline_package.tgz ./ol8_offline_package.tgz

# 3. 删除临时容器
docker rm temp-container
