# fnhugo

飞牛系统上的 Hugo 站点 - 庞老师的实验田。

## 技术栈

- 飞牛 fnOS(Debian 12 bookworm)
- [Hugo](https://gohugo.io/) v0.146.0+
- [PaperMod](https://github.com/adityatelange/hugo-PaperMod) v8.0 (作为子模块)
- GitHub Pages 托管

## 仓库结构

```
fnhugo/
├── content/           # 内容
│   ├── posts/        # 博客文章
│   ├── about.md      # 关于页
│   └── archives/     # 归档
├── static/           # 静态资源
├── themes/
│   └── PaperMod/     # PaperMod 子模块
├── hugo.toml         # 站点配置
└── README.md
```

## 快速开始

```bash
# 克隆(含子模块)
git clone --recurse-submodules https://github.com/mrpjmx/fnhugo.git
cd fnhugo

# 本地预览
hugo server -D

# 构建生产版本
hugo --minify
```

## 部署

部署到 GitHub Pages:
1. 设置 `hugo.toml` 中 `baseURL = "https://mrpjmx.github.io/fnhugo/"`
2. push 代码到 `master` 分支
3. GitHub Actions 自动构建并部署

## PaperMod 主题

本仓库使用 [PaperMod](https://github.com/adityatelange/hugo-PaperMod) 作为子模块。

要更新 PaperMod 到最新版本:

```bash
cd themes/PaperMod
git pull origin master
cd ../..
git add themes/PaperMod
git commit -m "chore: update PaperMod"
```

## License

代码采用 MIT 协议。内容采用 CC BY-NC-SA 4.0。

---

_Author: 庞老师_