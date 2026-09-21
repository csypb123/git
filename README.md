# 🚗 3D 汽车模型（Three.js）

一个使用 **Three.js** 构建的交互式 3D 跑车模型，支持在浏览器中实时旋转、缩放、换色，并带有丰富的细节和动画效果。

> 🌐 在线预览：<https://csypb123.github.io/git/>

## ✨ 功能特性

### 模型细节
- **车身**：引擎盖、座舱、后备箱、前后保险杠（圆角处理）
- **车头**：进气格栅（镀铬横条）、贯穿式日行灯带、双透镜大灯、雾灯
- **车尾**：贯穿式尾灯、双出排气管、碳纤维扩散器
- **外观套件**：碳纤维尾翼、轮拱、侧裙、前唇、鲨鱼鳍天线
- **玻璃**：前/后挡风玻璃、侧窗、三角窗、天窗、后视镜镜面
- **车轮**：双五辐轮毂、轮辋外圈、刹车盘、红色刹车卡钳（不随车轮转动）
- **车牌**：Canvas 动态生成的文字车牌「3D·CAR」

### 动画效果
- 🚗 自动绕圈行驶（车头始终朝切线方向）
- 🔄 车轮滚动 + 前轮转向（阿克曼转角）
- 🎢 车身姿态：转弯侧倾、加速俯仰、行驶颠簸
- 💨 排气管烟雾粒子系统
- 🚪 车门绕铰链平滑开合
- 💡 前照灯 SpotLight 光束投射（可开关）
- 🔄 视角自动旋转

### 交互操作
| 操作 | 说明 |
|------|------|
| 鼠标拖拽 | 旋转视角 |
| 滚轮 | 缩放 |
| 右键拖拽 | 平移视角 |
| 底部按钮 | 切换 5 种车漆颜色 |
| 底部按钮 | 视角旋转 / 行驶停止 / 开关车门 / 前照灯 |

## 🚀 本地运行

方式一：直接双击打开 `car-model.html`（需联网加载 Three.js CDN）。

方式二：使用任意静态服务器：

```bash
# Python
python -m http.server 8080
# 然后访问 http://localhost:8080

# Node.js (npx)
npx serve .
```

## 📁 文件结构

```
.
├── car-model.html                # 3D 汽车模型主文件
├── index.html                    # GitHub Pages 首页（iframe 嵌入模型）
├── README.md                     # 项目说明
└── .github/
    └── workflows/
        └── deploy-pages.yml      # GitHub Pages 自动部署
```

## 🛠️ 技术栈

- [Three.js](https://threejs.org/) v0.160 — WebGL 3D 渲染
- OrbitControls — 视角控制器
- RoundedBoxGeometry — 圆角几何体
- 原生 ES Modules（importmap 加载 CDN 依赖）

## 📦 部署到 GitHub Pages

本项目已配置 GitHub Actions 自动部署，操作步骤如下：

1. 打开仓库 **Settings → Pages**
2. 在 **Build and deployment → Source** 中选择 **GitHub Actions**
3. 之后每次推送到 `main` 分支，都会自动构建并部署
4. 部署完成后访问：<https://csypb123.github.io/git/>

## 📄 许可证

MIT License — 可自由使用和修改。
