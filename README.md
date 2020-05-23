# gitbook-plugin-copyright-v 👋

[![NPM Version](https://img.shields.io/npm/v/gitbook-plugin-copyright-v.svg)](https://www.npmjs.com/package/gitbook-plugin-copyright-v)
[![NPM Download](https://img.shields.io/npm/dt/gitbook-plugin-copyright-v.svg)](https://www.npmjs.com/package/gitbook-plugin-copyright-v)
[![License: MIT](https://img.shields.io/npm/l/gitbook-plugin-copyright-v.svg)](https://github.com/crazycodeboy/gitbook-plugin-copyright-v/blob/master/LICENSE)
[![Github: crazycodeboy](https://img.shields.io/badge/github-crazycodeboy-brightgreen.svg)](https://github.com/crazycodeboy)

> `gitbook-plugin-copyright-v` 是基于Gitbook实现的**版权保护插件**,用于复制内容时**追加版权信息**以及文章末尾**添加版权小尾巴**.


## 特色

- 支持复制内容**自动追加**版本保护信息
- 支持文章末尾**自动生成**版本保护尾巴
- 支持自定义小尾巴**版权保护图片**
- 支持 `Gitbook` **多语言环境**


## 🚀 用法

### Step #1 - 更新 `book.json` 配置文件

1. 在 `book.json` 配置文件中,添加 `copyright` 到 `plugins` 列表.
2. 在 `book.json` 配置文件中,配置 `pluginsConfig` 对象.

#### 单语言版简单示例 `book.json`

```json
{
    "plugins": ["copyright-v"],
    "pluginsConfig": {
        "copyright-v": {
            "site": "https://crazycodeboy.github.io/gitbook-plugin-copyright-v",
            "author": "Test",
            "website": "Test",
            "image": "https://crazycodeboy.github.io/crazycodeboy-wechat-open.png",
            "copyProtect": false
        }
    }
}
```

#### 多语言版简单示例 `book.json`

```json
{
    "plugins": ["copyright-v"],
    "pluginsConfig": {
        "copyright-v": {
            "site": "https://crazycodeboy.github.io/gitbook-plugin-copyright-v",
            "author": {
                "en": "crazycodeboy",
                "zh": "Test"
            },
            "website": {
                "en": "crazycodeboy's Gitbook",
                "zh": "Test"
            },
            "image": {
                "en": "image url",
                "zh": "image url"
            },
            "copyProtect": false
        }
    }
}
```

其中,配置参数含义如下:

- `site` : [必选]部署网站基本路径
- `author` : [必选]作者信息
- `website` : [必选]网站名称
- `image` : [可选]版权保护图片
- `copyProtect` : [可选]复制内容是否追加版权保护信息
- `enableFooter` : [可选]是否在页脚追加版权保护信息

### Step #2 - 运行 gitbook 相关命令

- 运行 `gitbook install` 命令安装到本地项目

```bash
$ gitbook install
```

- 运行 `gitbook build` 命令构建本地项目或者 `gitbook serve` 启动本地服务.

```bash
$ gitbook build
```

或者

```bash
$ gitbook serve
```
