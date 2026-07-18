# Gaussian Cloud Bungee Simulator / 高斯云蹦极模拟器

[![Itch.io Demo](https://img.shields.io/badge/Itch.io-Live%20Demo-fa5c5c?logo=itch.io&logoColor=white)](https://fqgame.itch.io/gausbungeesim)
[![GitHub License](https://img.shields.io/github/license/alexVirtualWorld/bungee)](https://github.com/alexVirtualWorld/bungee/blob/main/LICENSE)
[![Git LFS](https://img.shields.io/badge/Git-LFS-fee3d1?logo=git-lfs&logoColor=white)](https://git-lfs.github.com/)

---

### **[English Description]**

Experience the absolute thrill of bungee jumping in *any* 3D environment!

**Gaussian Cloud Bungee Simulator** is a cutting-edge web-based physics simulation game that leverages revolutionary **3D Gaussian Splatting (3DGS)** technology. It transforms standard static 3D scans into dynamic, immersive jump zones.

The core highlight is the unparalleled customizability: you are not confined to pre-built levels. In the starter menu, you can load your own online map URLs or select local `.splat`, `.ply`, or `.spz` files. Furthermore, you can utilize the real-time **"Scene Adjustment"** panel to perfectly align the virtual bungee platform with your custom environment and then export this perfect setup as a `.json` configuration file for convenient sharing.

#### 🚀 Technical Highlights
*   **Engine:** Based on Three.js, rendering through standard WebGL.
*   **3DGS Integration:** Uses the `@mkkellogg/gaussian-splats-3d` library for high-performance point cloud rendering.
*   **Physics Simulation:** Dynamic bungee rope physics, air drag, and realistic camera FOV effects based on velocity.
*   **Multilingual Support:** Fully localized in English, Simplified Chinese, Japanese, and Korean.

---

### **[中文介绍]**

在*任何* 3D 环境中体验绝对刺激的蹦极！

**高斯云蹦极模拟器** 是一款前沿的网页端物理模拟游戏，利用了革命性的 **3D 高斯渲染（3DGS）** 技术。它将标准的静态 3D 扫描模型转化为动态、沉浸式的跳跃区域。

核心亮点在于无与伦比的自定义特性：你不再被限制在预建的关卡中。在启动菜单中，你可以加载自己的在线地图 URL 或选择本地 `.splat`、`.ply` 或 `.spz` 文件。此外，你还可以使用实时 **“场景调整”** 面板，让虚拟蹦极平台与你的自定义环境完美贴合，然后将这一完美设置导出为 `.json` 配置文件，方便分享。

#### 🚀 技术亮点
*   **引擎:** 基于 Three.js，通过标准 WebGL 渲染。
*   **3DGS 集成:** 使用 `@mkkellogg/gaussian-splats-3d` 库进行高性能点云渲染。
*   **物理模拟:** 动态蹦极绳索物理、空气阻力以及基于速度的真实摄像机视场角（FOV）效果。
*   **多语言支持:** 完美支持中（简体）、英、日、韩四国语言。

---

## 🗺️ How to Run Locally / 如何在本地运行

### [English]
Since this project fetches large Gaussian Splat files, browsers prohibit direct opening from the local file system (e.g., `file://`) due to CORS security policies. You **must** run it using a local web server.

1.  **Node.js/npm:**
    ```bash
    npx serve .
    # Then open http://localhost:5000 in your browser
    ```
2.  **VS Code:** Install the **"Live Server"** extension, open the project folder, and click "Go Live" in the bottom status bar.
3.  **Python:**
    ```bash
    python -m http.server
    # Then open http://localhost:8000 in your browser
    ```

### [中文]
由于该项目需要拉取大型高斯文件，出于跨域（CORS）安全策略的考虑，浏览器禁止从本地文件系统（即 `file://`）直接打开 `index.html`。你**必须**使用本地 Web 服务器来运行。

1.  **Node.js/npm:**
    ```bash
    npx serve .
    # 然后在浏览器中打开 http://localhost:5000
    ```
2.  **VS Code:** 安装 **"Live Server"** 扩展，打开项目文件夹，点击底部状态栏的 "Go Live"。
3.  **Python:**
    ```bash
    python -m http.server
    # 然后在浏览器中打开 http://localhost:8000
    ```

---

## 🎮 Controls / 操作指南

| Action / 动作 | Control / 控件 |
| :--- | :--- |
| **Enter Scene / 进入场景** | Start Menu -> Click "**▶ Click here to enter scene / ▶ 点击此处进入场景**" |
| **Look Around / 环顾四周** | Move mouse / 移动鼠标 |
| **Jump / 起跳** | Lock camera and press **`SPACE` (空格键)** |
| **Reset / 重置状态** | Press **`R`** to return to platform / 按 **`R` 键** 返回平台 |
| **Unlock Mouse / 解锁鼠标** | Press **`ESC`** (Also brings back the transformation panel / 也会唤出变换面板) |

> ⚠️ **IMPORTANT NOTE ON IMPORTING JSON:** When you use the "**📥 Import Map Params / 📥 导入地图参数**" feature, the file is only added to your "Saved Maps" list. It will **NOT** immediately take effect. You **MUST** find the map in the list below and manually click the "**Load / 载入**" button next to it.
>
> ⚠️ **关于导入 JSON 的重要提示：** 当您使用“**📥 导入地图参数**”功能时，该文件仅会被添加至下方的“快捷选择已有地图”列表中，**并不会立即生效**。您导入成功后，**必须**在地图列表中找到该地图，并手动点击旁边的 **“载入”** 按钮，参数才会真正生效。

---

## 📦 Large File Notice (Git LFS) / 大文件说明

### [English]
Due to the large size of the custom `.splat`, `.ply`, and `.spz` map files, this repository utilizes **Git Large File Storage (LFS)**. To download the actual map data, you **MUST** have Git LFS installed on your machine before cloning the repository.

**How to Clone correctly:**
1.  **Install Git LFS:** Visit [https://git-lfs.github.com/](https://git-lfs.github.com/) and download the client. Run `git lfs install` once.
2.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/alexVirtualWorld/bungee.git](https://github.com/alexVirtualWorld/bungee.git)
    cd bungee
    # The map data will automatically pull down in the background.
    ```

### [中文]
由于自定义 `.splat`、`.ply` 和 `.spz` 地图文件的体积较大，该存储库利用了 **Git Large File Storage (LFS)** 技术。如果你希望正确下载到实际的地图数据，你**必须**在克隆（clone）仓库之前，先在本地机器上安装 Git LFS。

**如何正确克隆：**
1.  **安装 Git LFS:** 访问 [https://git-lfs.github.com/](https://git-lfs.github.com/) 下载客户端。运行一次 `git lfs install` 命令。
2.  **克隆仓库:**
    ```bash
    git clone [https://github.com/alexVirtualWorld/bungee.git](https://github.com/alexVirtualWorld/bungee.git)
    cd bungee
    # 地图数据将在后台自动同步下载。
