# DeltaForce OBS Lockhead Plugin v2.6.1 — 电脑端 & 手机端

> **状态：UD (未检测)** | 基于 YOLOv11 目标检测 | OBS 虚拟摄像头画面吸附

---

## 🎥 手机端演示

<div align="center">
  <img src="https://raw.githubusercontent.com/ace-trump-tech/DeltaForce-Locker/main/Mobile/demo_video.gif" alt="手机端功能演示" width="400">
  <br>
  <em>手机端 APK 画面吸附 / 模拟输入演示</em>
</div>

---

## 🚀 获取项目

![Star -> Fork -> Download 流程示意图](https://raw.githubusercontent.com/ace-trump-tech/DeltaForce-Locker/main/Mobile/demo.png)

1. **Star** — 点击右上角 Star 按钮
2. **Fork** — Fork 到自己的 GitHub 账号
3. **Download** — Code → Download ZIP 下载

> 电脑端代码位于 `Desktop/`，手机端位于 `Mobile/`。

---

## 📦 项目构成

| 平台 | 技术栈 | 入口 | 文档 |
|------|--------|------|------|
| **电脑端** | Python, PyQt5, YOLOv11, OBS | `python gui.py` | [Desktop/Readme.md](./Desktop/Readme.md) |
| **手机端** | Android APK | `Mobile/download_apk.py` | [Mobile/Readme.md](./Mobile/Readme.md) |

---

## 🎯 电脑端功能

### 自瞄 (Aimbot)
YOLOv11n ~ YOLOv11x 多模型可切换，支持头部/胸部优先、自动压枪、无后坐力、掩体检测、FOV 10°~360° 可调、1~100 级平滑度、自定义键盘/鼠标热键。

### 视觉 (Visuals)
方框透视、骨骼显示、玩家名称、血量条、距离显示。

### 杂项 (Misc)
雷达显示、十字准星叠加。

### 特性
- PyQt5 原生蓝白主题 GUI，多标签页配置
- 自定义 TTF 字体渲染
- 按键捕获绑定
- OBS 虚拟摄像头画面采集
- GPU 加速推理 (CUDA)

---

## 📚 教程

> **👉 [三角洲行动腾讯管家吸附原理](https://blog.csdn.net/qq_63129682/article/details/161447283)**
> **👉 [手把手教你注册GitHub账号](https://blog.csdn.net/qq_63129682/article/details/161460238)**
> **👉 [从零开始：两种主流方式轻松部署Python开发环境](https://blog.csdn.net/qq_63129682/article/details/161473936)**

---

## 🚨 版本更新 (v2.6.1)

- PyQt5 重构 GUI，多标签页（自瞄/视觉/杂项/关于）
- 集成 YOLOv11n/s/m/l/x 模型实时切换
- 热键捕获系统（键盘+鼠标按键）
- 自定义字体渲染
- 优化注入流程与状态提示

### 历史版本
| 版本 | 技术演进 |
|------|---------|
| V1.x | 基础 YOLO 检测 + OBS 捕获 + 鼠标模拟 |
| V2.x | 动态路径隐藏、光斑视觉中心算法、多帧投票 |
| V2.6 | PyQt5 重构、多标签 GUI、YOLOv11 集成 |

---

## 📄 许可证

MIT License

*最后更新：2026-06-18*
