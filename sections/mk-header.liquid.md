# MK 导航头部组件

> 版本：1.0.0  
> 作者：崽崽 (AI助手)  
> 基于：mypetcustom mk-header.liquid, whale ug-header.liquid  

---

## 功能特性

- ✅ **Logo 管理**：支持图片 Logo 和文字 Logo，可配置位置（居左/居中/居右）
- ✅ **MegaMenu 支持**：通过 Block 配置，支持两种模式（基础/图片）
- ✅ **透明头部**：支持首页、产品页、集合页启用透明效果
- ✅ **粘性头部**：支持始终固定和向上滚动时显示两种模式
- ✅ **移动端适配**：完整的移动端抽屉菜单
- ✅ **搜索 & 购物车**：可配置的快捷操作按钮

---

## 文件结构

```
sections/
└── mk-header.liquid          # 主头部组件

snippets/
├── mk-mega-menu-desktop.liquid           # PC端 MegaMenu
├── mk-mega-menu-desktop-image.liquid      # PC端图片 MegaMenu
└── mk-mega-menu-mobile.liquid            # 移动端 MegaMenu
```

---

## 使用方法

### 1. 基本配置

在 Shopify 后台的主题编辑器中，找到「MK 导航头部」区块进行配置：

- **主菜单**：选择一个已创建的菜单链接列表
- **Logo**：上传品牌 Logo 图片
- **菜单位置**：选择菜单在 Logo 的哪一侧

### 2. 配置 MegaMenu

在头部区块的「区块」选项卡中，点击「添加区块」：

#### Mega Menu 菜单

```
触发菜单项: Shop          ← 必须与菜单项名称完全匹配
标题: 新品上市
描述: 探索最新系列产品
链接文字: 查看全部
链接地址: /collections/new
```

#### Mega Menu 图片菜单

同上配置，并额外添加：

```
图片: [选择图片]
图片标题: 2024春季系列
图片链接文字: 立即选购
图片链接地址: /collections/spring-2024
```

### 3. 透明头部

在「透明头部」设置中启用：

- ☑️ 首页启用透明头部
- ☑️ 产品页启用透明头部
- ☑️ 集合页启用透明头部

---

## Schema 设置项

### Settings

| 设置项 | 类型 | 默认值 | 说明 |
|--------|------|--------|------|
| `logo` | Image | - | Logo 图片 |
| `logo_width` | Range | 120px | PC端 Logo 宽度 |
| `logo_width_mobile` | Range | 100px | 移动端 Logo 宽度 |
| `logo_position` | Select | left | Logo 位置 |
| `menu` | LinkList | main-menu | 主菜单 |
| `menu_position` | Select | center | 菜单位置 |
| `enable_transparent_header_home` | Checkbox | false | 首页透明头部 |
| `enable_transparent_header_product` | Checkbox | false | 产品页透明头部 |
| `enable_transparent_header_collection` | Checkbox | false | 集合页透明头部 |
| `enable_sticky_header` | Select | none | 粘性效果 |
| `section_height` | Select | default | 头部高度模式 |
| `show_search` | Checkbox | true | 显示搜索 |
| `show_cart` | Checkbox | true | 显示购物车 |
| `background_color` | Color | #ffffff | 背景颜色 |
| `text_color` | Color | #1a1a1a | 文字颜色 |

### Blocks

#### mega_menu

| 设置项 | 类型 | 说明 |
|--------|------|------|
| `trigger` | Text | 触发菜单项名称 |
| `title` | Text | 标题 |
| `description` | Textarea | 描述文字 |
| `link_text` | Text | 链接文字 |
| `link_url` | Url | 链接地址 |

#### mega_menu_image

| 设置项 | 类型 | 说明 |
|--------|------|------|
| `trigger` | Text | 触发菜单项名称 |
| `title` | Text | 标题 |
| `description` | Textarea | 描述文字 |
| `image` | Image | 图片 |
| `image_title` | Text | 图片标题 |
| `image_link_text` | Text | 图片链接文字 |
| `image_link_url` | Url | 图片链接地址 |

---

## CSS 变量

```css
:root {
  --mk-header-height: 70px;
  --mk-header-height-compact: 56px;
  --mk-header-z-index: 100;
}
```

### 可覆盖变量

| 变量 | 说明 |
|------|------|
| `--header-bg` | 头部背景颜色 |
| `--header-text` | 头部文字颜色 |
| `--padding-top` | 上内边距 |
| `--padding-bottom` | 下内边距 |
| `--logo-width-desktop` | PC端 Logo 宽度 |
| `--logo-width-mobile` | 移动端 Logo 宽度 |

---

## JavaScript API

### HeaderComponent

```javascript
// 监听头部加载完成
document.addEventListener('header:loaded', (e) => {
  console.log('Header initialized', e.detail);
});
```

### 方法

| 方法 | 说明 |
|------|------|
| `toggleMobileMenu()` | 切换移动端菜单 |
| `closeMobileMenu()` | 关闭移动端菜单 |

---

## 迁移记录

### v1.0.0 (2026-04-12)
- 初始版本，从 mypetcustom 和 whale 项目迁移
- 整合了两者的最佳实践
- 支持 MegaMenu 和透明/粘性头部

---

## 相关组件

- [mk-mega-menu-desktop.liquid](../snippets/mk-mega-menu-desktop.liquid.md)
- [mk-mega-menu-desktop-image.liquid](../snippets/mk-mega-menu-desktop-image.liquid.md)
- [mk-mega-menu-mobile.liquid](../snippets/mk-mega-menu-mobile.liquid.md)
