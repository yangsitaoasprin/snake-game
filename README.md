# 🐍 Snake Game

一个经典的贪吃蛇游戏，使用纯 HTML5、CSS3 和 JavaScript 开发。

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 📋 项目简介

这是一个复古风格的贪吃蛇游戏。游戏目标是控制蛇吃掉食物，随着游戏进行蛇的身体会变长，需要避免撞到墙壁或蛇的身体。

### 🎮 游戏特性

- **经典玩法**: 原汁原味的贪吃蛇游戏体验
- **响应式设计**: 支持各种屏幕尺寸
- **流畅动画**: 使用 requestAnimationFrame 实现高性能游戏循环
- **计分系统**: 实时显示得分和当前速度等级
- **难度递增**: 随着得分提高，游戏速度会增加
- **简洁界面**: 清爽的游戏UI，易于上手
- **键盘控制**: 支持方向键或 WASD 键操作

---

## 🚀 快速开始

### 系统要求

- 现代浏览器（Chrome、Firefox、Safari、Edge 等）
- 支持 HTML5 Canvas

### 安装和运行

1. **克隆仓库**：
```bash
git clone https://github.com/yangsitaoasprin/snake-game.git
cd snake-game
```

2. **打开游戏**：
直接在浏览器中打开 `snake-game.html` 文件即可开始游戏

```bash
# Windows
start snake-game.html

# macOS
open snake-game.html

# Linux
xdg-open snake-game.html
```

或者在浏览器地址栏中输入文件路径。

---

## 🎯 游戏规则

### 基本规则

1. **目标**: 控制蛇吃掉食物（红色方块），每吃一个食物得 10 分
2. **蛇的增长**: 每次吃掉食物后，蛇的身体会增长一节
3. **游戏结束**:
   - 蛇撞到游戏边界
   - 蛇撞到自己的身体
4. **难度**: 随着分数增加，游戏速度会逐步提高

### 得分规则

| 事件 | 得分 |
|------|------|
| 吃掉食物 | +10 分 |
| 速度等级每提升 1 级 | 基础得分 +5 分 |

---

## 🎮 操作方式

### 键盘控制

| 按键 | 功能 |
|------|------|
| ⬆️ `Up Arrow` 或 `W` | 向上移动 |
| ⬇️ `Down Arrow` 或 `S` | 向下移动 |
| ⬅️ `Left Arrow` 或 `A` | 向左移动 |
| ➡️ `Right Arrow` 或 `D` | 向右移动 |
| `Space` 或点击游戏界面 | 暂停/继续 |
| `R` 或点击"重新开始" | 重新开始游戏 |

---

## 📊 游戏界面

```
┌─────────────────────────────────┐
│  Snake Game                     │
│  Score: 100  | Level: 2         │
├─────────────────────────────────┤
│                                 │
│         🐍 🐍 🐍                │
│             🍎                  │
│                                 │
├─────────────────────────────────┤
│  [暂停] [重新开始]              │
└─────────────────────────────────┘
```

---

## 💻 技术栈

- **HTML5**: Canvas API 用于游戏绘制
- **CSS3**: 样式和布局
- **JavaScript (ES6+)**:
  - 面向对象编程（OOP）
  - requestAnimationFrame 实现游戏循环
  - 事件处理
  - 碰撞检测算法

### 核心代码结构

```javascript
// 蛇对象
class Snake {
  constructor() { ... }
  move() { ... }
  grow() { ... }
  checkCollision() { ... }
}

// 食物对象
class Food {
  constructor() { ... }
  spawn() { ... }
}

// 游戏管理器
class Game {
  constructor() { ... }
  update() { ... }
  render() { ... }
  gameLoop() { ... }
}
```

---

## 🎨 游戏配置

你可以在代码中修改以下参数来自定义游戏：

```javascript
// 游戏配置
const CONFIG = {
  GRID_SIZE: 20,              // 网格大小（像素）
  GAME_WIDTH: 400,            // 游戏宽度
  GAME_HEIGHT: 400,           // 游戏高度
  INITIAL_SPEED: 100,         // 初始速度（毫秒）
  MIN_SPEED: 50,              // 最小速度
  SPEED_INCREASE: 2,          // 每级速度增加量
};
```

---

## 🏆 高分挑战

目标：
- 🥉 **初级**: 得分 100+
- 🥈 **中级**: 得分 500+
- 🥇 **高级**: 得分 1000+
- 🏅 **传奇**: 得分 2000+

---

## 🐛 已知问题

- 移动时的反向移动检测：蛇不能直接反向移动（向左时不能立即向右）

---

## 🔄 版本历史

### v1.0.0 (2025-12-25)
- ✅ 初始版本发布
- ✅ 基础游戏逻辑实现
- ✅ 计分和难度系统
- ✅ 暂停/继续功能
- ✅ 响应式界面设计

---

## 🤝 贡献

欢迎贡献代码！如果你想改进游戏：

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

### 建议的改进方向

- [ ] 添加声音效果
- [ ] 实现排行榜（本地存储）
- [ ] 添加不同难度模式
- [ ] 实现游戏皮肤/主题切换
- [ ] 添加特殊道具（加速、减速、盾牌等）
- [ ] 实现联网多人对战

---

## 📝 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

---

## 👨‍💻 作者

- **开发者**: Yang Sitao
- **GitHub**: [@yangsitaoasprin](https://github.com/yangsitaoasprin)

---

## 📧 联系方式

如有问题或建议，欢迎提交 Issue 或联系我：

- 📧 Email: yangsitaoasprin@gmail.com
- 🐙 GitHub Issues: [提交 Issue](https://github.com/yangsitaoasprin/snake-game/issues)

---

## 🙏 致谢

感谢所有玩家的支持和反馈！

---

**enjoy the game!** 🎮🎉

