
---

# 微聊系统 (mini_chat)

> **挨过雨的人，总想给别人打一把伞。**  
> **不希望每个人都被雨淋过，但希望他们能早点找到归宿。**

---

## 📸 赛博起源

[![封号记录](https://raw.githubusercontent.com/Pjjush16/mini_chat/e2dfdcc39c209059121484e9c40d48001172efd2/Screenshot_20260621_231633.jpg)](https://raw.githubusercontent.com/Pjjush16/mini_chat/e2dfdcc39c209059121484e9c40d48001172efd2/Screenshot_20260621_231633.jpg)

2026年6月21日，我因为一句 **“普通人访问全球互联网都能干些什么呢？”**，被千问封禁了账号。  
系统重复了三次同样的回复：

> **“抱歉，系统检测您的账号存在异常风险，目前已停止使用。”**

我没有申诉，也没有回头。我卸载了它，然后用连续的时间，把曾经想用的功能，全部写进了这个开源项目里。

这就是那扇把我关在门外的门。  
**所以，我重新开了一扇。**

---

## ✨ 核心特性

### 🧠 AI 智能体
- 工具调用（时间/计算/联网搜索/用户信息）
- LaTeX 图层绘图（支持 `!level` 分层叠加）
- OCR 图像识别（云端 API 与本地 Tesseract 双保险降级）
- 系统级语音输入与流式音频合成

### 💬 即时通讯
- 好友系统、群聊系统（支持频道模式与匿名发言）
- WebRTC 点对点加密通信
- 消息高亮、消息撤回（内置扩容卡机制）
- 拼手气红包、礼物赠送、转账系统

### 🪙 经济与奖励
- 微聊币钱包：每日签到、交易记录
- 消费商店：改名卡、撤回扩容卡、幸运抽奖
- 快应用打赏与内购（平台抽成 10%，90% 归开发者）
- 成就系统与经验等级

### ⚡ 快应用生态
- 用户可上传 HTML 快应用（类似小程序）
- 内置内购 API 与打赏面板
- 播放量统计与开发者收益看板

---

## 🎬 快速部署

### 环境要求
- PHP 7.4+
- MySQL 5.7+ / MariaDB 10.2+
- PDO 扩展
- WebRTC 推荐 HTTPS 环境

### 安装步骤

```bash
# 1. 下载源码
git clone https://github.com/Pjjush16/mini_chat.git
cd mini_chat

# 2. 在根目录创建 config.php
# 参考以下格式：
```

config.php 示例

```php
<?php
define('DB_HOST', 'localhost');
define('DB_NAME', 'weiliao_db');
define('DB_USER', 'root');
define('DB_PASS', 'your_password');

define('SITE_NAME', '微聊');
define('SITE_LOGO', '/logo.png');

define('AI_NAME', '万象');
define('AI_AVATAR', '/ai_avatar.png');
define('AI_SYSTEM_PROMPT', '你是一个智能助手...');

define('RTC_CONFIG', json_encode([
    'iceServers' => [
        ['urls' => 'stun:stun.l.google.com:19302']
    ]
]));
?>
```

---

##🔧 工具调用示例

AI 通过 【tool】 和 【/tool】 标记调用内置工具：

```json
【tool】
{"tool":"get_current_time"}
【/tool】

【tool】
{"tool":"calculate","expression":"1024 * 768"}
【/tool】

【tool】
{"tool":"search_web","query":"今天上海天气"}
【/tool】

【tool】
{"tool":"get_user_info"}
【/tool】
```

---

##🎨 LaTeX 图层绘图示例

支持通过 【photo】 和 【/photo】 绘制分层图形：

```text
【photo】
!rect 0 6 10 4 blue level0
!rect 0 0 10 6 green level0
!sun 8 8 1.5 yellow level1
!text 5 9 large white Hello level2
【/photo】
```

支持图形：
!heart、!star、!smile、!sun、!rect、!circle、!text

支持图层： level 参数（数字越小越底层）

---
##🎵 音乐生成示例

通过 【audio】 标记生成音乐：

```text
【audio】
!bpm 120
!track piano
C4 0.5
D4 0.5
E4 0.5
C4 0.5
【/audio】
```

支持乐器：
piano、violin、cello、harp、flute、trumpet、sax、guitar、organ、bell、drum、snare、hihat、timpani

---

##📜 授权哲学

这把伞应该保护人，而不是变成另一场雨。

· 🔒 核心代码：AGPLv3
    如果你将此系统部署为公共网络服务，你必须完整开源修改代码，并继续沿用 AGPLv3 许可。
· 🍃 个人与自用：MIT 豁免
    如果你是个人开发者，或搭建非盈利、非公开的私人环境，我以个人名义授权你按 MIT 许可 使用。不限制修改，不要求开源，只需保留原始署名。

---

##💬 联系

如果你愿意，可以把这个伞撑到更远的地方。
或者只是聊聊天：

📧 yaoqingxuan20221@outlook.com

---

这里没有任何封号原则。不管你传递什么，都是自由的。

⚙️ 由 一个多情又无情的人 撰写。

