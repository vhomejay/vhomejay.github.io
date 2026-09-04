---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 16b7bc9fc94e20a304dbfebfe1d20e00_88950e60a7a211f199d2525400287e28
    ReservedCode1: O7Kb9Gew4S4iAkSK2RbImH0ud+VNC6Fapgi0Nvctvx1QXP66EjYZf3aiURtY3EKzSC1tUWERqSSjbV7ISFJCBAn2ptDYjrNQN1Xs0bcRUr2cZhPOR5fUXOI0Nqc5ewuECfZ3QlnabyNVZlMU4wbmunEFxGoJHo2TP8BRMftq5MSv9fCL12wSZptXi3U=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 16b7bc9fc94e20a304dbfebfe1d20e00_88950e60a7a211f199d2525400287e28
    ReservedCode2: O7Kb9Gew4S4iAkSK2RbImH0ud+VNC6Fapgi0Nvctvx1QXP66EjYZf3aiURtY3EKzSC1tUWERqSSjbV7ISFJCBAn2ptDYjrNQN1Xs0bcRUr2cZhPOR5fUXOI0Nqc5ewuECfZ3QlnabyNVZlMU4wbmunEFxGoJHo2TP8BRMftq5MSv9fCL12wSZptXi3U=
---

# videos/ — 视频本地托管占位目录

本目录用于存放作品集视频文件，**视频本地托管**（不上传第三方平台），由站点页面直接引用本地相对路径播放。

## 目录结构约定（14 个作品格，按公司分组）

```
videos/
├── README.md                      ← 本说明文件（可保留）
├── work-jgp-01.mp4 ~ work-jgp-06.mp4   # S-01 交个朋友优选科技有限公司（6 格）
│     jgp-01 / jgp-02                  → 交个朋友直播间
│     jgp-03 / jgp-04                  → 交个朋友食品直播间
│     jgp-05 / jgp-06                  → TikTok Shop 东南亚跨境电商
├── work-dky-01.mp4 ~ work-dky-04.mp4  # S-02 厦门市都可赢文化传媒有限公司（4 格）
│     dky-01 / dky-02                  → 悦秀大酒楼（豆干嬷）
│     dky-03 / dky-04                  → 阿里元老宋
├── work-zl-01.mp4 ~ work-zl-02.mp4    # S-03 厦门紫龙信息服务有限公司（2 格）
│     zl-01 / zl-02                    → 短视频混剪 · 拍剪一体
└── work-ywl-01.mp4 ~ work-ywl-02.mp4  # S-04 莆田市易万莱电子商务有限公司（2 格）
      ywl-01 / ywl-02                  → 影视二创 · 节奏短片
```

公司缩写：`jgp`=交个朋友（优选科技） · `dky`=都可赢 · `zl`=紫龙 · `ywl`=易万莱

## 命名规范

- 文件名必须与 `index.html` 中每个作品卡片 `data-src` 的路径**完全一致**（当前共 14 个作品格）。
- 建议格式：`work-<公司缩写>-<序号>.mp4`，避免空格与特殊字符。
- 视频未放入时，页面显示渐变占位封面，点击会提示待上传状态并回退占位。

## 编码要求（GitHub Pages 托管关键）

GitHub Pages 单文件大小限制为 **100MB**，且需要浏览器可直接播放：

| 项目 | 推荐值 |
| --- | --- |
| 封装格式 | MP4（H.264 + AAC） |
| 分辨率 | 1920×1080 或 1280×720 |
| 码率 | 视频 ≤ 4 Mbps，音频 128 kbps |
| 单文件大小 | 建议 ≤ 50MB（越小加载越快） |

推荐压缩命令（macOS 已内置 ffmpeg 时）：

```bash
ffmpeg -i 原始素材.mp4 -c:v libx264 -crf 23 -preset medium \
       -c:a aac -b:a 128k -movflags +faststart -vf scale=1280:-2 \
       videos/work-jgp-01.mp4
```

## 替换步骤

1. 将压缩后的 mp4 按命名规范放入本目录；
2. 刷新页面即可在对应作品格播放（无需改代码）。
*（内容由AI生成，仅供参考）*
