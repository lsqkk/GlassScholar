# GlassScholar

[![LICENSE](https://img.shields.io/github/license/yaoyao-liu/minimal-light?style=flat-square&logo=creative-commons&color=EF9421)](https://github.com/yaoyao-liu/minimal-light/blob/main/LICENSE)

`GlassScholar` 是一个基于 [Minimal Light](https://github.com/yaoyao-liu/minimal-light) 深度改造的学术主页模板仓库，适合用作公开 demo、二次开发起点，或直接 Fork 成你自己的学术主页。

当前仓库已经去除了原始个人信息，默认内容全部替换为虚构人物、虚构项目、虚构教育经历与虚构动态，便于安全公开展示。

## 这个 demo 里有什么

- `About / Education / Projects / Awards / Skills / News` 六个主要模块
- `_config.yml` 控制站点标题、头像、模块开关、仓库看板等全局配置
- `_data/*.yml` 驱动所有示例内容，方便整体替换
- 保留时间轴、卡片、毛玻璃、图片弹窗、暗色模式等现有视觉与交互特性

## 安全说明

- 当前示例人物 `Dr. Ivy Chen` 为虚构角色
- 仓库中的项目、事件、学校、奖项、论文、服务信息均为演示用途
- 头像已改为 Wikimedia Commons 的公开图片链接
- 旧的个人简历 PDF、旧生成页面、旧自定义域名配置已从仓库中移除

## 快速开始

1. Fork 本仓库
2. 修改 `_config.yml`
3. 按需编辑 `_data/profile.yml`、`_data/education.yml`、`_data/project.yml`、`_data/awards.yml`、`_data/news.yml`
4. 在 GitHub Pages 中启用部署

本地预览：

```bash
bundle install
bundle exec jekyll serve --livereload
```

默认访问地址：

```text
http://127.0.0.1:4000/
```

## 主要内容文件

```text
_config.yml
_data/profile.yml
_data/education.yml
_data/project.yml
_data/awards.yml
_data/news.yml
_data/publications.yml
_data/services.yml
index.md
```

## 建议你接下来替换的地方

- 姓名、职位、单位、邮箱、头像
- 教育经历与研究方向
- 项目、论文、奖项、新闻
- GitHub 仓库看板配置

## 致谢

本项目基于以下开源工作：

- [yaoyao-liu/minimal-light](https://github.com/yaoyao-liu/minimal-light)
- [pages-themes/minimal](https://github.com/pages-themes/minimal)
- [orderedlist/minimal](https://github.com/orderedlist/minimal)
- [al-folio](https://github.com/alshedivat/al-folio)
