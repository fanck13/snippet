# 使用一个Ubuntu为基础镜像
FROM ubuntu:latest

# 更新包列表
RUN apt-get update && \
    apt-get install -y software-properties-common curl gnupg2

# 添加CMake PPA源以便获取特定版本
RUN curl -sSL https://apt.kitware.com/keys/kitware-archive-latest.asc | gpg --dearmor -o /usr/share/keyrings/kitware-archive-keyring.gpg && \
    echo "deb [signed-by=/usr/share/keyrings/kitware-archive-keyring.gpg] https://apt.kitware.com/ubuntu/ $(lsb_release -cs) main" > /etc/apt/sources.list.d/kitware.list

# 安装指定版本的CMake
RUN apt-get update && \
    apt-get install -y cmake=3.21.* # 替换为你要安装的具体版本号

# 清理缓存
RUN rm -rf /var/lib/apt/lists/*