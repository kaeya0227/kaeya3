# Kaeya Literature Radar


## 文件结构

```text
index.html
assets/kaeya-birthday-2023.png
data/latest.json
data/runs.json
data/archive/2026-06-07.json
config/interests.json
```

## 数据更新方式

网页默认读取：

```text
data/latest.json
```

如果这个文件暂时读取失败，网页会退回到 HTML 内置的示例数据，避免页面空白。

历史归档页会读取：

```text
data/runs.json
```

只要 `runs.json` 里记录了某天的归档路径，例如 `data/archive/2026-06-07.json`，网页上的日期就可以点击，并会载入那一天保存下来的完整文献卡片。

每天自动化应该更新：

```text
data/latest.json
data/archive/YYYY-MM-DD.json
data/runs.json
```

## GitHub Pages

GitHub Pages 地址：

```text
https://你的用户名.github.io/你的新仓库名/
```

仓库设置应为：

```text
Settings -> Pages -> Source -> Deploy from a branch
Branch -> main
Folder -> / (root)
```

## Codex 自动化目标

每天上午 9 点，Codex 自动化应：

1. 检索 NBER、SSRN、arXiv、英文期刊、中文期刊等来源。
2. 筛选约 20 篇经济学、金融学、管理学相关论文。
3. 生成中文文献卡片；每篇都按完整精读摘要标准写清研究动机、研究背景、数据来源、创新之处、具体文章内容、机制路径、主要发现、与你的关系和证据边界。
4. 不编造论文、作者、链接、摘要或结论。
5. 只更新 `data/*.json`。

## 版权提示

凯亚主题图仅用于个人非商业学习页展示。若页面未来用于公开传播、论文项目主页或商业用途，建议改成自制/授权图片或抽象冰元素背景。
