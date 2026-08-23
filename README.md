# 开心消消乐 · Three.js

用 Three.js 实现的 3D 三消游戏：8×8 棋盘、6 种手工建模的动物头（猫 / 狗 / 猪 / 熊 / 青蛙 / 兔子）、连锁消除、粒子特效，以及用 Web Audio API 实时合成的背景音乐与音效。

## 玩法

- 点击一个动物，再点击相邻动物进行交换
- 横 / 竖 3 个及以上相同动物连成一线即可消除
- 消除后上方动物下落并补充新动物，自动连锁，连击有分数加成
- 20 步内尽可能得高分；无解时自动洗牌

## 运行

```bash
npm install
npm run dev
```

打开 http://localhost:5173 。

构建生产版本：

```bash
npm run build
```

## 技术

- [Three.js](https://threejs.org/) — 场景、灯光、阴影、射线拾取
- [Vite](https://vitejs.dev/) — 开发与构建
- Web Audio API — 无外部素材的音乐与音效合成（`src/audio.js`）

## 结构

```
index.html        页面与 HUD
src/main.js       游戏逻辑、动物建模、动画、渲染
src/audio.js      音乐与音效
src/style.css     样式
```
