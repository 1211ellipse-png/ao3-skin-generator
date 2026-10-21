# AO3 Work Skin 调试

帮助写workskill用的 skill，帮同人女编写和调试 Work Skin（自定义 CSS 皮肤），步骤如下：问清需求 → 生成 CSS + 正文 HTML → 根据反馈或 AO3 报错进行修改。

## 主要的功能如下

- 生成聊天框、信件/日记、彩色台词、排版美化、整篇主题皮肤；
- 生成互动样式：点击展开隐藏文字（`details`）、悬停显示、装饰文字、有限动画；
- 输出**符合 AO3 HTML/CSS 白名单**的代码，避免被 AO3 报错；
- 按 AO3 报错定位问题并给替代写法；

## 安装

### Codex CLI

把整个 `ao3-work-skin` 文件夹复制到 skills 目录：

```
~/.codex/skills/
```

即最终路径为 `~/.codex/skills/ao3-work-skin/SKILL.md`。（若你的 Codex 版本使用其他路径，以官方文档为准。）

### Claude Code

把整个 `ao3-work-skin` 文件夹复制到：

```
~/.claude/skills/
```

即最终路径为 `~/.claude/skills/ao3-work-skin/SKILL.md`。

## 使用

装好后，直接用自然语言进行描述即可：

- 「帮我把这段对话做成微信聊天框皮肤」
- 「我想写一个点击就能展开隐藏剧透的样式」
- 「给我一个蓝白色的信件样式」

代理会自动问 2–3 个关键问题，然后输出三段内容：① Work Skin CSS、② 正文 HTML、③ 使用说明。

## 示例输出

```
### ① Work Skin CSS
.wsk-chat { max-width: 30em; }
.wsk-msg { padding: 0.5em; border-radius: 0.5em; }

### ② 正文 HTML
<div class="wsk-chat">
  <p class="wsk-msg"><strong>A:</strong> 你在吗？</p>
</div>

### ③ 使用说明
1. AO3 → Skins → My Work Skins → Create Work Skin → 贴① → Submit
2. 发帖时 Work Skin 下拉框选这个皮肤
3. 正文切 HTML 编辑器，贴②，点 Preview
```

## 许可

CC0 —— 可自由使用、修改、转发。开源、开源、开源。

## 免责

输出以 AO3 官方规则为准，使用前请在自己作品里测试。
