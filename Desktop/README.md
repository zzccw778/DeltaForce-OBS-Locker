# DeltaForce-OBS-Locker —— 手把手教学（电脑端）

> 📘 **这是一份完整的 Python 编程 & 计算机视觉实战教程**  
> 通过跟随本教程，你将学会：  
> - 🐍 Python 开发环境的标准配置（虚拟环境、依赖管理）  
> - 🖼️ OpenCV / YOLO 图像识别的基本流程  
> - 🖱️ 模拟输入 API 的调用方法（`SendInput`、`pyautogui`）  
> - 🔌 OBS 插件机制与渲染 Hook 原理  
> - 🧪 对抗反作弊系统的基础思路
> 
> 👉 **[三角洲行动腾讯管家吸附原理&本项目 v3 版本介绍](https://blog.csdn.net/qq_63129682/article/details/161447283)**  

> ⚙️ **Python 环境部署教程（必读）**：如果还没有安装 Python，请先完成 **[Python 环境部署教程](https://blog.csdn.net/qq_63129682/article/details/161460238)**。

---

## 📥 安装方式 —— 手把手配置 Python 环境

1. **获取代码**  
   ```bash
   git clone https://github.com/ace-trump-tech/DeltaForce-OBS-Locker.git
   cd DeltaForce-OBS-Locker/desktop
创建虚拟环境（Windows）

bash
python -m venv venv
venv\Scripts\activate
安装依赖

bash
pip install -r requirements.txt
如果下载慢，可换国内镜像：pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

运行

bash
python gui.py
或

bash
python main.py
🎮 使用方法
启动游戏（仅用于观察算法效果，请勿在真实对局中使用）。

运行 gui.py 或 main.py。

按 F9 启用演示模式，程序会打印敌人头部坐标并移动鼠标。

按 F10 停止。

💡 调试模式：修改 config.yaml 中的 show_bone: true，可在屏幕上绘制识别到的骨骼点。

🛠 代码结构解析（学习地图）
text
desktop/
├── config.yaml             # 配置文件 → YAML 解析
├── requirements.txt        # 依赖列表
├── main.py                 # 主入口（无界面）
├── gui.py                  # 图形化界面
├── creat_logger.py         # 日志工厂
├── downloader.py           # 模型下载器
├── fake_plugin.py          # 伪装插件逻辑（DLL 劫持演示）
├── notifier.py             # 系统通知
├── data/
│   └── bin/crypto.py       # Base64 编码/解码（反静态分析演示）
├── models/
│   ├── weights/            # 预训练权重
│   ├── detector.py         # YOLO 检测器
│   ├── preprocess.py       # 预处理
│   ├── postprocess.py      # 后处理（NMS）
│   └── utils.py            # IOU、锚框计算
└── utils/
    ├── logger.py           # 日志装饰器
    ├── registry.py         # 注册器
    └── test_downloader.py  # 单元测试
推荐学习顺序：

环境准备 → requirements.txt, venv

运行 gui.py → 观察界面与日志

理解配置与日志 → config.yaml, creat_logger.py

核心识别流程 → models/detector.py, preprocess.py, postprocess.py

模拟输入与热键 → main.py 中的热键回调

反检测技巧 → data/bin/crypto.py, fake_plugin.py

单元测试 → utils/test_downloader.py

❓ 常见问题
问题	解决方法
pip install 报错	换用国内镜像源，或检查网络。
ModuleNotFoundError	虚拟环境未激活或依赖未安装。
程序闪退	查看控制台报错，检查日志。
鼠标乱动	调低 config.yaml 中的 sensitivity。
杀毒软件报警	添加白名单；这是模拟输入的正常行为。
找不到模型权重	运行 downloader.py 自动下载。
📌 法律与道德提醒
🚨 本项目唯一的合法使用场景是：本地学习、教学演示、反作弊技术研究。
严禁在任何真实游戏对局中使用！ 使用类似技术可能导致账号永久封禁。
我们提供代码的目的是帮助你掌握 Python 编程、图像识别和模拟输入等技能，而不是教你作弊。

6L+Z5Liq6aG555uu55qE5pys6LSo5YW25a6e5piv5Y+N5L2c5byK6aG555uu77yM6K+l6aG555uu5a6e6ZmF6L+Q6KGM5ZCO5Lya5biu5L2g5LiL6L2944CK5pqX5Yy656qB5Zu044CL6L+Z5Liq5ri45oiP5bm25LiU5o+Q6YaS5L2g5Y2D5LiH5LiN6KaB5bCd6K+V5L2c5byK77yB5LiO5YW26L+Z5qC36LS55bC95b+D5oCd5Zyw56C05Z2P5ri45oiP55qE5YWs5bmz5oCn6L+Y5LiN5aaC6Lef5oiR5LiA6LW35a2m5LmgcHl0aG9u5oqA6IO95ZKMZ2l0aHVi55qE5Z+65pys55+l6K+G5ZGi

📄 许可证
MIT License —— 可自由修改，但严禁用于商业作弊软件。

*最后更新：2026-06-09*
