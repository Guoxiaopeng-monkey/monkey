# MK MegaMenu Mobile 组件

> 版本：1.0.0  
> 作者：崽崽 (AI助手)  
> 基于：mypetcustom mk-mega-menu-mobile.liquid  

---

## 功能说明

移动端抽屉菜单中的 MegaMenu 组件，使用 Accordion 展开/收起形式。

**特点**：
- 手风琴展开效果
- 支持图片展示
- 触摸友好

---

## 使用方法

```liquid
{% render 'mk-mega-menu-mobile', mega_menu_block: block, link: link, link_handle: link.handle %}
```

---

## 参数

| 参数 | 类型 | 必需 | 说明 |
|------|------|------|------|
| `mega_menu_block` | Block | 是 | 来自 header 区间的 block 对象 |
| `link` | Link | 是 | 父级链接对象 |
| `link_handle` | String | 否 | 链接的处理名称，用于生成唯一 ID |

---

## 示例

```liquid
{% for link in menu_links %}
  {% assign mega_menu_block = null %}
  {% for block in section.blocks %}
    {% if block.type == 'mega_menu' %}
      {% if block.settings.trigger == link.title %}
        {% assign mega_menu_block = block %}
      {% endif %}
    {% endif %}
  {% endfor %}
  
  {% if mega_menu_block %}
    {% render 'mk-mega-menu-mobile', mega_menu_block: mega_menu_block, link: link %}
  {% else %}
    <li>...</li>
  {% endif %}
{% endfor %}
```

---

## 展开效果

```
┌─────────────────────────┐
│  Collections        ▼  │  ← 点击展开
├─────────────────────────┤
│  精选系列                 │
│  发现适合你风格的产品系列   │
│                         │
│  [图片]                   │
│                         │
│  立即选购 →              │
└─────────────────────────┘
```

---

## 相关资源

- [mk-header.liquid](../sections/mk-header.liquid.md)
- [mk-mega-menu-desktop.liquid](./mk-mega-menu-desktop.liquid.md)
- [mk-mega-menu-desktop-image.liquid](./mk-mega-menu-desktop-image.liquid.md)
