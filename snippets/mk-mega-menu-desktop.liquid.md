# MK MegaMenu Desktop 组件

> 版本：1.0.0  
> 作者：崽崽 (AI助手)  
> 基于：mypetcustom mk-mega-menu-desktop.liquid  

---

## 功能说明

PC 端 MegaMenu 下拉菜单组件，用于头部导航中。

**特点**：
- 只显示配置的内容（标题、描述、链接）
- 不显示子菜单项
- 鼠标悬停时平滑显示

---

## 使用方法

```liquid
{% render 'mk-mega-menu-desktop', mega_menu_block: block, link: link %}
```

---

## 参数

| 参数 | 类型 | 必需 | 说明 |
|------|------|------|------|
| `mega_menu_block` | Block | 是 | 来自 header 区间的 block 对象 |
| `link` | Link | 否 | 父级链接对象（可选） |

---

## 示例

### 基础用法

```liquid
{% for block in section.blocks %}
  {% if block.type == 'mega_menu' %}
    {% assign link_title_stripped = link.title | strip %}
    {% assign block_trigger_stripped = block.settings.trigger | strip %}
    {% if block_trigger_stripped == link_title_stripped %}
      {% render 'mk-mega-menu-desktop', mega_menu_block: block, link: link %}
    {% endif %}
  {% endif %}
{% endfor %}
```

### 完整配置

Header 区间配置：

```json
{
  "type": "mega_menu",
  "settings": {
    "trigger": "Shop",
    "title": "新品上市",
    "description": "探索最新系列产品，发现独特设计",
    "link_text": "查看全部",
    "link_url": "/collections/new"
  }
}
```

---

## 样式类

| 类名 | 说明 |
|------|------|
| `.mk-mega-menu` | MegaMenu 容器 |
| `.mk-mega-menu__content` | 内容区域 |
| `.mk-mega-menu__title` | 标题 |
| `.mk-mega-menu__description` | 描述 |
| `.mk-mega-menu__link` | 链接按钮 |
| `.mk-mega-menu__arrow` | 箭头图标 |

---

## 效果演示

```
┌─────────────────────────────────┐
│  Shop ▼  │  About  │  Contact  │  🔍  🛒
└─────────────────────────────────┘
              │
              ▼ hover
         ┌──────────────────┐
         │   新品上市        │
         │  探索最新系列...   │
         │  查看全部 →       │
         └──────────────────┘
```

---

## 相关资源

- [mk-header.liquid](../sections/mk-header.liquid.md)
- [mk-mega-menu-desktop-image.liquid](./mk-mega-menu-desktop-image.liquid.md)
- [mk-mega-menu-mobile.liquid](./mk-mega-menu-mobile.liquid.md)
