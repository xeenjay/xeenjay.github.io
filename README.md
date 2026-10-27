# xeenjay.github.io

Xinjie Huang 的个人学术主页：https://xeenjay.github.io

基于 [Minimal Light](https://github.com/yaoyao-liu/minimal-light) 主题（CC0 协议），由 GitHub Pages 自动构建，不需要额外配置 Actions。

## 改哪里

| 想改的内容 | 文件 |
|---|---|
| 名字、发音、职位、学校、邮箱、GitHub 等链接 | `_config.yml` |
| About Me、Research Interests、Experience、Education | `index.md` |
| 研究项目列表（标题、导师、时间、简介、缩略图、链接） | `_data/research.yml` |
| 头像 | `assets/img/avatar.png` |
| 研究项目缩略图 | `assets/img/research/` |

在 GitHub 网页上点开文件，再点右上角的铅笔图标就能直接改，改完点 **Commit changes**，一两分钟后网站会自动更新。

## 换照片和缩略图

1. 在仓库页面打开 `assets/img`（头像）或 `assets/img/research`（缩略图）文件夹。
2. 点 **Add file → Upload files**，上传图片。文件名和原来的一样就会直接覆盖，比如头像就命名为 `avatar.png`。
3. 如果文件名不一样（比如上传的是 `.jpg` 或 `.gif`），记得同步修改 `_config.yml` 里的 `avatar:`，或 `_data/research.yml` 里对应项目的 `image:`。

头像建议用正方形照片，会自动裁成圆形。缩略图会裁成约 270 × 123 的横幅，所以宽图效果最好。视频生成的结果可以直接用 GIF。

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
