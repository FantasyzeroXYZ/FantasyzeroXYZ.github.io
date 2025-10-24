# 个人博客
## GitHub自动部署
* gh-deploy

## 虚拟环境以及对应依赖
* 创建虚拟环境
  * `python -m venv venv`
* 查看当前安装的python版本列表
  * `py --list`
* 指定python版本创建虚拟环境
  * `py -版本 -m venv venv`
    * 3.11.2
* 在目录下激活虚拟环境 
  * `.\venv\Scripts\Activate.ps1`
* 更新虚拟环境里的pip
  * `python -m pip install --upgrade pip`
* 退出虚拟环境
  * `deactivate`

* 生成requirements.txt
  * `pip freeze > requirements.txt`

* [mkdocs-material](https://github.com/squidfunk/mkdocs-material)
* mkdocs-blog-plugin
* mkdocs-rss-plugin
* 模板
  * [create-blog](https://github.com/mkdocs-material/create-blog)

* 本地预览(powershell)
  * `$env:PYTHONPATH = "$env:PYTHONPATH;$env:GITHUB_WORKSPACE"`
  * `mkdocs serve`

## 文件结构
```
├──.github/
│   └── workflows/
│       └── ci.yml          # GitHub自动部署脚本
├── docs/
│   ├── index.md
│   └── blog/
├── ext/
│   ├── __init__.py
│   └── slugs.py
├── hooks/
│   └── socialmedia.py
├── venv/                   # 虚拟环境目录
├──.gitignore
├── mkdocs.yml
├── README.md
└── requirements.txt        # 可选：依赖列表文件
```

## 待办
* [ ] tag分类
* [ ] 更新博客文章
* [ ] 界面中文化设置
* [ ] 搜索中文化设置
* [ ] 设置评论功能
* [ ] RSS

