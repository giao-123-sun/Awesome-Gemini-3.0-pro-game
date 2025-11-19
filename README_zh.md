# Awesome Gemini 3.0 Pro Game Collection

**[中文]** | [English]

## 📖 项目简介 (Introduction)

**Awesome Gemini 3.0 Pro Game Collection** 是一个探索 Web 技术极限与生成式 AI 深度融合的开源游戏实验项目。

我们的目标很简单：**在一个网页中，集成多种利用 AI 驱动的创新玩法。** 我们利用 Three.js/WebGL 处理高性能图形，利用 Gemini 3.0 Pro 等大模型作为游戏世界的“上帝引擎”，实时生成剧情、视觉素材（SVG/Pixel Art）和逻辑代码。

> **核心理念：** 游戏不应该只有预设好的内容。你的 API Key 就是通往无限世界的钥匙。

-----

## 🎮 游戏列表 (Game List)

我们目前正在并行开发以下核心游戏模组：

### 1\. ⚔️ Sky Voxel Drifter (天际方块漂移)

  * **类型：** 3D 动作 / 跑酷
  * **核心玩法：** 高性能的网页版“Minecraft + 鞘翅飞行”。体验极致的空气动力学，使用烟花加速，在程序化生成的浮空岛屿间穿梭。
  * **技术栈：** Three.js, Cannon.js (物理引擎)。
  * ![Alt Text](./svger//sky-voxel.svg)

### 2\. 🌌 The Infinite Text Dungeon (无限文字地牢)

  * **类型：** AI Native RPG / 交互式小说
  * **核心玩法：**
      * 一个没有边界的文字冒险游戏。你的每一个离谱操作（“试图说服史莱姆投资比特币”）都会被 AI 合理化并推动剧情。
      * **实时视觉化：** 每次场景描述更新时，AI 会实时生成一张像素风格的背景图，增强沉浸感。
  * **API 配置 (BYOK):**
      * 用户需在设置面板提供 `API Key`, `Base URL`, `Model Name`。
      * 支持接入 OpenAI, Anthropic, 或任何兼容 OpenAI 格式的 Local LLM。
  * **降级模式 (Fallback Mode):**
      * 如果没有提供 API Key，游戏将自动切换到\*\*“精选剧本模式”\*\*。
      * 玩家将在预设好的、高质量的静态分支剧情中进行游玩（不消耗 Token，但剧情有限）。
       * ![Alt Text](./svger/text-dungeon.svg)

### 3\. 🏙️ Dream City Builder (梦境城市)

  * **类型：** 放置建造 / 生成式 UI
  * **核心玩法：**
      * **Text-to-City：** 你输入描述（例如：“一座建立在巨大的发光蘑菇上的赛博朋克城市”）。
      * **Gemini 3.0 驱动：** 游戏后端调用 Gemini 3.0 Pro，直接输出复杂的 **SVG 代码**。
      * 网页前端实时渲染这些 SVG，构建出独一无二的建筑物和装饰物。
  * **技术点：** 利用 LLM 强大的代码生成能力来替代传统的 3D建模流程。
  *  * ![Alt Text](./svger/city-builder.svg)

### 4\. ☯️ Karma Flow (流年：天命肉鸽)

  * **类型：** 生辰八字 Roguelike
  * **核心玩法：**
      * **八字即构筑：** 开局随机生成生辰八字，五行（金木水火土）决定了你的基础属性和技能卡组。
      * **大运流年：** 每一关代表一岁，你需要利用五行生克原理，在“流年不利”时存活，在“大运助身”时爆发。
  * **技术栈：** Lunar-javascript, Pixi.js。
 * ![Alt Text](./svger/karma-flow.svg)
-----

## ⚙️ 架构与配置 (Architecture & Config)

本项目采用 **"AI-Optional"** 架构。核心游戏逻辑在本地运行，AI 特性通过 API 增强。

### 全局设置面板 (Global Settings)

在网页右上角，点击 ⚙️ 图标可打开配置：

```json
{
  "ai_provider": "custom", // or "gemini", "openai"
  "base_url": "https://generativelanguage.googleapis.com/v1beta/openai/",
  "api_key": "sk-proj-...",
  "model_name": "gemini-1.5-pro-latest",
  "image_generation_enabled": true
}
```

  * **连接状态：** 🟢 已连接 / 🔴 离线（将使用本地降级模式）

-----

## 🚀 快速开始 (Getting Started)

```bash
# 1. 克隆项目
git clone https://github.com/your-username/awesome-gemini-game.git

# 2. 进入目录
cd awesome-gemini-game

# 3. 安装依赖
npm install

# 4. 启动本地服务器
npm run dev
```

打开浏览器访问 `http://localhost:3000` 即可开始体验。

-----