# 使用 Node 22 镜像
FROM node:22

# 设置工作目录
WORKDIR /app

# 复制 package.json 和 package-lock.json
COPY frontend/package*.json /app/

# 仅删除 node_modules，保留 package-lock.json
RUN rm -rf node_modules

# 使用 npm ci 安装依赖（确保版本一致性）
RUN npm i --include=dev

# 复制前端项目的其他文件
COPY frontend /app/

# 启动前端开发服务器
CMD ["npm", "run", "dev"]
