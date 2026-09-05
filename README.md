# 💍 婚礼邀请函 H5

微信可打开的婚礼邀请函（单页 H5：封面 → 配乐 → 倒计时 → 照片轮播 → 婚礼信息）。
在线地址见仓库 Pages：`https://bily1258-design.github.io/wedding-invitation/`

## 怎么改内容（不用懂代码）

编辑 `index.html` 顶部 **配置区 CONFIG** 一处即可：

| 配置 | 含义 | 当前值 |
|---|---|---|
| `groom` / `bride` | 新郎 / 新娘称呼 | 新郎 / 新娘 |
| `date` | 婚礼时间（倒计时用，格式 `年/月/日 时:分`） | 2026/10/03 18:00 |
| `dateTxt` | 页面上显示的时间文案 | 2026 年 10 月 3 日 |
| `venue` | 场地名 | 江西老宅 |
| `addr` | 详细地址（空则不显示，复制按钮只复制场地名） | （空） |
| `invite` | 邀请正文（`<br>` 换行） | 默认文案 |
| `photos` | 照片文件路径列表 | assets/photos/1~4.jpg |

## 素材放哪

```
assets/
  music.mp3      ← 背景配乐（放任意 mp3，建议 ≤ 2MB）
  photos/
    1.jpg ~ 4.jpg ← 照片，竖版 4:5 效果最佳（建议压缩到 ≤ 300KB/张）
```

照片不存在时页面自动显示"照片待放"占位卡，不会报错；放入后刷新即显示。
音乐文件缺失时静默跳过，不影响浏览。

## 提交后生效

```bash
cd ~/wedding-invitation
git add -A && git commit -m "update" && git push
```

GitHub Pages 约 1 分钟内自动更新，微信内直接打开链接即可（可加屏保/浮窗转发给宾客）。
