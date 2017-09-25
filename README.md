# hexo-theme-mip

Hexo MIP 模板, [在线预览](https://xuexb.github.io/hexo-theme-mip-demo/)

## 安装

```bash
# 安装依赖
npm install --save \
    hexo-browsersync \
    hexo-renderer-jade \
    hexo-generator-feed \
    hexo-generator-sitemap \
    hexo-generator-archive \
    hexo-generator-mip

# 克隆主题
git clone https://github.com/xuexb/hexo-theme-mip.git themes/mip
```

> 注意: [hexo-generator-mip](https://github.com/xuexb/hexo-generator-mip) 模块会处理 MIP 规范的标签, 如抽离 `<style>`、处理 `<a>` 标签、处理 `<img>` 标签, 如果不使用 Hexo MIP 相关模板, 请不要安装该模块


## 配置

修改 `_config.yml` 的 `theme` 配置项为 `mip`:

```yaml
# 站点信息
title: '网站首页标题'
subtitle: '网站二级页面标题后缀'
description: '网站描述'
author: '网站作者, 导航和版权使用'
url: '网站绝对 http 链接'
language: zh-cn

# 启用 mip 主题
theme: mip

# 在归档页面显示所有文章
# 需要上面安装的 hexo-generator-archive 插件支持
archive_generator:
    per_page: 0
    yearly: false
    monthly: false
    daily: false
```


## 使用

### 插入图片

由于 [MIP img标签规范](https://www.mipengine.org/examples/mip/mip-img.html) , 在使用图片时必须设置宽高, 如:

```html
<img src="https://dummyimage.com/100x100" width="100" height="100" alt="desc">
```

### 摘要

在文单合适位置插入 `<!-- more -->` 将提取为主页的摘要文本

### 描述

- 首页使用 `config.description`
- 文章页使用 `post.desc` , 如果不存在则使用 `post.title + config.author`

### 警告块

思路来自 [@pinggod/hexo-theme-apollo](https://github.com/pinggod/hexo-theme-apollo) , 颜色来自 [layui](http://www.layui.com/doc/element/color.html)

#### 默认 - 绿色

```html
<div class="tip">
    预处理器很强大，但它只是编写 CSS 的辅助工具。出于对扩展和维护等方面的考虑，在大型项目中有必要使用预处理器构建 CSS；但是对于小型项目，原生的 CSS 可能是一种更好的选择。不要肆意使用预处理器！
</div>
```

#### 提示 - 蓝色

```html
<div class="tip-info">
    预处理器很强大，但它只是编写 CSS 的辅助工具。出于对扩展和维护等方面的考虑，在大型项目中有必要使用预处理器构建 CSS；但是对于小型项目，原生的 CSS 可能是一种更好的选择。不要肆意使用预处理器！
</div>
```

#### 警告 - 红色

```html
<div class="tip-error">
    预处理器很强大，但它只是编写 CSS 的辅助工具。出于对扩展和维护等方面的考虑，在大型项目中有必要使用预处理器构建 CSS；但是对于小型项目，原生的 CSS 可能是一种更好的选择。不要肆意使用预处理器！
</div>
```

## todo

- [ ] 标签页
- [ ] 搜索页

## contributors

- [@yugasun](https://github.com/yugasun/)
- [@xuexb](https://github.com/xuexb/)

## License

[MIT](./LICENSE)
