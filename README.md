# 📋 反馈话术生成器 - 进度管理

一个用于生成反馈话术并跟踪处理进度的网页应用。

## ✨ 功能特点

- **话术生成**：根据选项自动生成反馈话术
- **进度追踪**：记录网管名称，跟踪附件提交和光路拆除进度
- **下一步提醒**：勾选待处理项后自动显示下一步操作
- **超期提醒**：自动计算并显示超期天数
- **数据持久化**：使用 LocalStorage 保存数据

## 🚀 部署方式

### 方式一：Vercel（推荐）

1. 将整个 `kimicode` 文件夹拖拽到 [Vercel](https://vercel.com/new) 网站
2. 自动识别配置并部署
3. 获得在线访问链接

或使用 Vercel CLI：
```bash
npm i -g vercel
vercel
```

### 方式二：Netlify

1. 将整个 `kimicode` 文件夹拖拽到 [Netlify Drop](https://app.netlify.com/drop)
2. 自动部署完成
3. 获得在线访问链接

### 方式三：Docker 部署

```bash
# 构建镜像
docker build -t feedback-tracker .

# 运行容器
docker run -d -p 8080:80 --name feedback-tracker feedback-tracker

# 或使用 docker-compose
docker-compose up -d
```

访问：http://localhost:8080

### 方式四：静态服务器

```bash
# 使用 Python
python -m http.server 8000

# 使用 Node.js
npx serve .

# 使用 PHP
php -S localhost:8000
```

### 方式五：Nginx 部署

将文件夹内容复制到 Nginx 的 html 目录：
```bash
sudo cp -r . /var/www/html/feedback-tracker/
```

或使用提供的 nginx.conf：
```bash
sudo cp nginx.conf /etc/nginx/conf.d/feedback-tracker.conf
sudo nginx -s reload
```

## 📁 文件说明

```
kimicode/
├── index.html          # 主页面
├── vercel.json         # Vercel 部署配置
├── netlify.toml        # Netlify 部署配置
├── Dockerfile          # Docker 镜像配置
├── docker-compose.yml  # Docker Compose 配置
├── nginx.conf          # Nginx 配置
├── package.json        # Node.js 项目配置
└── README.md           # 项目说明
```

## 💻 本地开发

直接在浏览器中打开 `index.html` 即可使用。

或使用本地服务器：
```bash
npm install
npm start
```

## 🔧 技术栈

- HTML5
- CSS3
- Vanilla JavaScript
- LocalStorage 数据存储

## 📱 浏览器支持

- Chrome / Edge / Firefox / Safari 最新版本
- 移动端浏览器
