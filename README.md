---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 16b7bc9fc94e20a304dbfebfe1d20e00_87f202bba7a211f1b87f525400461939
    ReservedCode1: fBHQQT6tp+hnZ6CagX99VIxdDmb97T3pjLWTJfDeSGR2ELOWRORVB0F+H4ITF4K/LH5Fc58/lDGD9+zkPf+mDARv+0qGgBY0GjZBeX/UmkkZApIWV0VweRLUIgqHmCTuTEEisMn5EOmu4zFEEE4c2up/lI22arO4ykhuQMdUos4DXul/zZqmjRpUnoY=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 16b7bc9fc94e20a304dbfebfe1d20e00_87f202bba7a211f1b87f525400461939
    ReservedCode2: fBHQQT6tp+hnZ6CagX99VIxdDmb97T3pjLWTJfDeSGR2ELOWRORVB0F+H4ITF4K/LH5Fc58/lDGD9+zkPf+mDARv+0qGgBY0GjZBeX/UmkkZApIWV0VweRLUIgqHmCTuTEEisMn5EOmu4zFEEE4c2up/lI22arO4ykhuQMdUos4DXul/zZqmjRpUnoY=
---



# vhomejay · 个人视频简历站

单页滚动式个人视频简历站（视频剪辑方向），**纯静态零依赖**：一个 HTML 文件内联全部 CSS/JS，无任何外部资源、字体或 CDN，开箱即用。

## 目录结构

```
output/
├── index.html          # 站点入口（单文件，含全部样式与脚本）
├── videos/             # 视频本地托管占位目录
│   └── README.md       # 视频命名规范 + 压缩参数说明
└── README.md           # 本说明
```

## 站点结构（单页滚动）

1. **Hero**：姓名（魏宏捷）+ 意向（编导运营剪辑/IP 操盘手）+ 简介 + 数据徽章 + 视频占位氛围
2. **作品集**：14 个作品格，按 4 家公司分组（交个朋友优选 6 / 都可赢 4 / 紫龙 2 / 易万莱 2），源为 `videos/work-<公司缩写>-NN.mp4` 占位
3. **经历**：时间线（4 段工作经历，公司名与职位与最新简历一致）
4. **技能**：剪辑后期 / 创作编导 / 运营增长 三组
5. **联系方式**：邮箱、账号名、地区、教育

## GitHub Pages 部署

1. 在 GitHub 创建仓库（如 `vhomejay.github.io` 或普通仓库 `<repo>`）；
2. 将 `index.html` 与 `videos/` 目录推送到仓库**根目录**：
   ```bash
   git init
   git add index.html videos/
   git commit -m "feat: personal video resume site"
   git branch -M main
   git remote add origin git@github.com:vhomejay/<repo>.git
   git push -u origin main
   ```
3. 打开仓库 **Settings → Pages**，Source 选择 `Deploy from a branch`，分支选 `main`、目录选 `/ (root)`，保存；
4. 访问 `https://vhomejay.github.io/<repo>/`（仓库名为 `vhomejay.github.io` 时直接访问 `https://vhomejay.github.io/`）。

## 本地预览

```bash
open index.html
```

## 接入真实视频

- 将成品视频放入 `videos/`，命名与压缩要求见 `videos/README.md`；
- 视频文件放入后刷新即可播放，无需修改 HTML；
- GitHub Pages 单文件上限 100MB，请务必先压缩（推荐 ≤50MB / 720p-1080p / H.264）。
*（内容由AI生成，仅供参考）*
*（内容由AI生成，仅供参考）*
