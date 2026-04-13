# MK MegaMenu Desktop Image 组件

> 版本：1.0.0  
> 作者：崽崽 (AI助手)  
> 基于：mypetcustom mk-mega-menu-desktop-image.liquid  

---

## 功能说明

PC 端带图片的 MegaMenu 下拉菜单组件，用于头部导航中。

**特点**：
- 左侧文字内容 + 右侧图片布局
- 支持图片标题和链接
- 响应式适配

---

## 使用方法

```liquid
{% render 'mk-mega-menu-desktop-image', mega_menu_block: block, link: link %}
```

---

## 参数

| 参数 | 类型 | 必需 | 说明 |
|------|------|------|------|
| `mega_menu_block` | Block | 是 | 来自 header 区间的 block 对象 |
| `link` | Link | 否 | 父级链接对象（可选） |

---

## 示例

```json
{
  "type": "mega_menu_image",
  "settings": {
    "trigger": "Collections",
    "title": "精选系列",
    "description": "发现适合你风格的产品系列",
    "link_text": "浏览全部",
    "link_url": "/collections",
    "image": "collection-banner.jpg",
    "image_title": "春季新品",
    "image_link_text": "立即选购",
    "image_link_url": "/collections/spring-2024"
  }
}
```

---

## 布局结构

```
┌─────────────────────────────────────────────┐
│  精选系列              ┌──────────────────┐  │
│  发现适合你风格...      │                  │  │
│  浏览全部 →            │    [图片]         │  │
│                        │   春季新品        │  │
└─────────────────────────────────────────────┘
```

---

## 相关资源

- [mk-header.liquid](../sections/mk-header.liquid.md)
- [mk-mega-menu-desktop.liquid](./mk-mega-menu-desktop.liquid.md)
- [mk-mega-menu-mobile.liquid](./mk-mega-menu-mobile.liquid.md)
