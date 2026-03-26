# 部署指南

## 方法一：部署到 Vercel（推荐）

1. 注册账号：https://vercel.com/
2. 安装 Vercel CLI：
```bash
npm install -g vercel
```
3. 在项目目录运行：
```bash
cd tools
vercel
```
4. 按提示操作，会自动部署并给你一个域名
5. 生产环境部署：
```bash
vercel --prod
```

## 方法二：部署到 Netlify

1. 注册账号：https://www.netlify.com/
2. 直接拖拽 `tools` 文件夹到 Netlify 网站即可
3. 或者使用 CLI：
```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod
```

## 方法三：GitHub Pages

1. 把项目推到 GitHub
2. 在仓库设置中开启 GitHub Pages
3. 选择 main 分支，根目录
4. 访问：https://username.github.io/repo-name/

## 方法四：自己的服务器

```bash
# 使用 Python
python3 -m http.server 8000

# 使用 Node.js
npx serve

# 使用 nginx（生产环境推荐）
# 配置反向代理到静态文件目录
```

## 部署后需要做的事

### 1. 修改域名
- 将 `yourdomain.com` 替换为你的实际域名
- 在 `index.html`, `robots.txt`, `sitemap.xml` 中修改

### 2. 申请 Google AdSense
1. 访问 https://www.google.com/adsense/
2. 注册账号，添加你的网站
3. 获取广告代码，替换 `index.html` 中的广告位
4. 等待审核通过（需要一定内容量和流量）

### 3. 提交到搜索引擎
- Google Search Console: https://search.google.com/search-console/
- 百度站长平台: https://ziyuan.baidu.com/
- 提交 sitemap.xml

### 4. 添加更多工具
可以继续添加更多工具来增加流量：
- URL 编解码
- 正则表达式测试
- 图片压缩
- PDF 工具
- 文本对比
- 等等

### 5. 数据统计
- 集成 Google Analytics
- 集成百度统计
- 分析用户行为，优化工具
