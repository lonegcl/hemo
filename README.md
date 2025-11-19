# 合末官网

基于 Vue 3 构建的现代化企业官网。

## 技术栈

- Vue 3
- Vue Router 4
- Vite
- 原生 CSS（响应式设计）

## 功能模块

1. **首页** - 公司logo、标语、banner展示
2. **公司简介** - 发展历程、经营范围、主要产品、核心竞争力、企业文化
3. **产品服务** - 买卖房垫资、银行转贷、企业信用过桥、电商供应链金融
4. **联系我们** - 公司地址、联系方式、工作时间、公众号二维码

## 安装和运行

### 安装依赖

```bash
npm install
```

### 开发模式

```bash
npm run dev
```

访问 http://localhost:3000

### 构建生产版本

```bash
npm run build
```

### 预览生产版本

```bash
npm run preview
```

## 项目结构

```
├── src/
│   ├── components/      # 公共组件
│   │   ├── NavBar.vue  # 导航栏
│   │   └── Footer.vue  # 页脚
│   ├── views/          # 页面组件
│   │   ├── Home.vue    # 首页
│   │   ├── About.vue   # 公司简介
│   │   ├── Services.vue # 产品服务
│   │   └── Contact.vue  # 联系我们
│   ├── router/         # 路由配置
│   ├── App.vue         # 根组件
│   ├── main.js         # 入口文件
│   └── style.css       # 全局样式
├── index.html
├── package.json
└── vite.config.js
```

## 注意事项

1. 请根据实际情况修改联系方式、地址等信息
2. 公众号二维码和抖音二维码需要替换为实际的二维码图片
3. 可以集成百度地图或高德地图显示公司位置
4. 建议替换 placeholder 中的 banner 图片为实际的公司宣传图

