# xeenjay.github.io

Xinjie Huang 的个人学术主页：https://xeenjay.github.io

基于 [Minimal Light](https://github.com/yaoyao-liu/minimal-light) 主题（CC0 协议），由 GitHub Pages 自动构建，不需要额外配置 Actions。

## 改哪里

| 想改的内容 | 文件 |
|---|---|
| 名字、发音、职位、学校、邮箱、GitHub 等链接 | `_config.yml` |
| About Me、Research Interests、Experience、Education | `index.md` |
| 研究项目列表（标题、导师、时间、简介、缩略图、链接） | `_data/research.yml` |
| 头像 | `assets/img/avatar.jpg` |
| 研究项目缩略图 | `assets/img/research/` |

在 GitHub 网页上点开文件，再点右上角的铅笔图标就能直接改，改完点 **Commit changes**，一两分钟后网站会自动更新。

## 换照片和缩略图

1. 在仓库页面打开 `assets/img`（头像）或 `assets/img/research`（缩略图）文件夹。
2. 点 **Add file → Upload files**，上传图片。文件名和原来的一样就会直接覆盖，比如头像就命名为 `avatar.jpg`。
3. 如果文件名不一样（比如上传的是 `.png` 或 `.gif`），记得同步修改 `_config.yml` 里的 `avatar:`，或 `_data/research.yml` 里对应项目的 `image:`。

头像建议用正方形照片，会自动裁成圆形。缩略图会裁成约 270 × 123 的横幅，所以宽图效果最好。

## 用视频当缩略图

视频生成的结果最适合用一小段视频展示。把 MP4 上传到 `assets/img/research/`，然后在 `_data/research.yml` 对应项目下加一行：

```yaml
    video: ./assets/img/research/world-rerenderer.mp4
```

视频会静音循环自动播放，加载完成前先显示 `image:` 那张图。建议截 3–6 秒、宽度 540 像素左右、文件控制在 2 MB 以内，否则页面会变慢。用 ffmpeg 压缩的参考命令：

```bash
ffmpeg -i input.mp4 -t 5 -vf "scale=540:-2" -an -c:v libx264 -crf 28 -movflags +faststart output.mp4
```

## 添加论文链接

在 `_data/research.yml` 对应项目下加上这几行（用不到的可以不写），页面上会出现对应的按钮：

```yaml
    pdf: https://arxiv.org/abs/xxxx.xxxxx
    code: https://github.com/xxx/xxx
    page: https://xxx.github.io/project/
```

## 本地预览（可选）

```bash
bundle install
bundle exec jekyll serve
```

然后打开 http://localhost:4000 。
