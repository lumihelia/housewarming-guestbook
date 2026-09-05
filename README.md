# Housewarming Guestbook / 新居留言簿

中文 · [English](./README.en.md)

一个为 2026 年 1 月 29 日新居宴做的轻量实时留言簿。

来宾写下名字和祝福后，留言会出现在同一面页面上，像一张张卡片挂在横杆上。点击卡片可以展开完整内容；新留言通过 Supabase Realtime 同步到页面。

[打开留言簿](https://housewarming-beige.vercel.app)

## 这个小页面

页面围绕一个很小的动作展开：写下一句祝福，让它挂到同一面留言墙上。

当前版本包含：

- 姓名与祝福留言；
- 按时间倒序展示已有留言；
- Supabase 实时同步新留言；
- 会轻微摆动的悬挂卡片；
- 点击卡片后展开完整留言与时间。

## 实现方式

整个项目集中在一个 `index.html` 中，没有构建步骤。

- **Tailwind CSS CDN**：页面布局与样式
- **Alpine.js**：表单、留言列表与弹窗交互
- **Supabase**：留言存储与 Realtime 更新
- **Google Fonts**：Playfair Display 与 Noto Serif TC
- **Vercel**：当前线上部署

数据表使用 `guestbook`，页面读取并写入 `name`、`message`、`created_at` 等字段。

## 仓库结构

```text
.
├── index.html
└── .gitignore
```

`index.html` 同时包含页面结构、样式和客户端逻辑，保留了这个一次性小项目最后运行时的完整形态。

## 当前状态

这个仓库更接近一份已经完成的数字小物件档案。最后一轮功能更新加入了悬挂卡片视觉和点击查看完整留言的弹窗，此后没有继续扩展成通用留言簿产品。
