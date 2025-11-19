# Awesome Gemini 3.0 Pro Game Collection

**[中文]** | [[English](./README.md)]

## 📖 项目简介 (Introduction)

**Awesome Gemini 3.0 Pro Game Collection** 是一个探索 Web 技术极限与生成式 AI 深度融合的开源游戏实验项目。

我们的目标很简单：**在一个网页中，集成多种利用 AI 驱动的创新玩法。** 我们利用 Three.js/WebGL 处理高性能图形，利用 Gemini 3.0 Pro 等大模型作为游戏世界的“上帝引擎”，实时生成剧情、视觉素材（SVG/Pixel Art）和逻辑代码。

> **核心理念：** 游戏不应该只有预设好的内容。你的 API Key 就是通往无限世界的钥匙。

-----

## 🎮 已上线游戏 (Playable Now)

以下游戏已包含完整的 HTML 文件，可直接在浏览器中运行。

### 1. ☯️ Karma Flow (流年：天命肉鸽)
**文件入口：** `game/KarmaFlow.html` (中文) / `game/KarmaFlow_en.html` (英文)

* **类型：** 生辰八字 Roguelike / 卡牌构筑
* **核心玩法：**
    * **八字即构筑：** 开局随机生成生辰八字，五行（金木水火土）决定了你的基础属性和技能卡组。
    * **大运流年：** 每一关代表一岁，你需要利用五行生克原理，在“流年不利”时存活，在“大运助身”时爆发。
* **立即试玩：**
    * [🀄 启动中文版](./game/KarmaFlow.html)
    * [🇺🇸 启动英文版](./game/KarmaFlow_en.html)

![Karma Flow](./svger/karma-flow.svg)

### 2. 🧪 Element AI (元素炼金实验室)
**文件入口：** `game/ElementChemistry.html` (中文) / `game/Chemlab.html` (英文)

* **类型：** AI 驱动合成 / 益智解谜
* **核心玩法：**
    * **无限合成：** 从基础元素开始，两两组合，合成宇宙万物。
    * **AI 裁决：** 与传统固定配方的合成游戏不同，**AI 实时判定**你的组合结果。它根据化学逻辑或天马行空的创意来生成新元素。
* **立即试玩：**
    * [🀄 启动中文版 (ElementChemistry)](./game/ElementChemistry.html)
    * *(备用中文版: [ElementAl](./game/ElementAl.html))*
    * [🇺🇸 启动英文版 (Chemlab)](./game/Chemlab.html)

### 3. ⚔️ Sky Voxel Drifter (天际方块漂移)
**文件入口：** `fly.html`

* **类型：** 3D 动作 / 跑酷
* **核心玩法：**
    * 高性能的网页版“Minecraft + 鞘翅飞行”模拟器。
    * 体验极致的空气动力学，使用烟花加速，在程序化生成的浮空岛屿间穿梭。
* **技术栈：** Three.js, Cannon.js (物理引擎)。
* **立即试玩：** [✈️ 启动飞行模拟器](./fly.html)

![Sky Voxel](./svger/sky-voxel.svg)

-----

## 🚧 开发中 (Roadmap)

以下模组正在积极研发中，敬请期待：

### 🌌 The Infinite Text Dungeon (无限文字地牢)
* **核心概念：** 一个没有边界的文字冒险游戏。你的每一个离谱操作（“试图说服史莱姆投资比特币”）都会被 AI 合理化并推动剧情，并实时生成像素背景图。
* **当前状态：** *Coming Soon*
![Text Dungeon](./svger/text-dungeon.svg)

### 🏙️ Dream City Builder (梦境城市)
* **核心概念：** Text-to-City 放置建造。后端调用 Gemini 3.0 Pro 直接输出复杂的 SVG 代码，前端实时渲染构建赛博朋克城市。
* **当前状态：** *Coming Soon*
![City Builder](./svger/city-builder.svg)

-----

## ⚙️ 架构与配置 (Architecture & Config)

本项目采用 **"AI-Optional"** 架构。核心游戏逻辑在本地运行，AI 特性通过 API 增强。

### 全局设置面板 (Global Settings)

在网页右上角（支持 AI 的游戏中），点击 ⚙️ 图标可打开配置：

```json
{
  "ai_provider": "custom", // or "gemini", "openai"
  "base_url": "[https://generativelanguage.googleapis.com/v1beta/openai/](https://generativelanguage.googleapis.com/v1beta/openai/)",
  "api_key": "sk-proj-...",
  "model_name": "gemini-1.5-pro-latest",
  "image_generation_enabled": true
}
````

  * **连接状态：** 🟢 已连接 / 🔴 离线（将使用本地降级模式）

-----

## 🚀 快速开始 (Getting Started)

由于这些是独立的 WebGL/HTML5 应用，您有两种方式运行：

### 方法 1: 直接游玩 (推荐)

直接进入文件夹，双击上述列表中的 `.html` 文件，使用浏览器（推荐 Chrome/Edge）打开即可游玩。

### 方法 2: 开发者模式

如果您需要修改代码或贡献：

```bash
# 1. 克隆项目
git clone [https://github.com/your-username/awesome-gemini-game.git](https://github.com/your-username/awesome-gemini-game.git)

# 2. 进入目录
cd awesome-gemini-game

# 3. 安装依赖
npm install

# 4. 启动本地服务器
npm run dev
```

# 打开浏览器访问 `http://localhost:3000` 即可开始体验。

```