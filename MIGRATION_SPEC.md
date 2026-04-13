# Monkey Theme 迁移规范

## 📋 迁移概述

从 poolin_store, whale, dyness_eu 三个项目中迁移定制组件到 monkey 主题。

### 源项目统计

| 项目 | 总sections | 定制组件 | 标准组件 |
|------|------------|----------|---------|
| poolin_store | 109 | ~70 spx-* | ~39 |
| whale | 107 | ~60 ug-* | ~47 |
| dyness_eu | 122 | ~80 spx-* | ~42 |
| **总计** | **338** | **~210** | **~128** |

### 迁移进度

| 组件类型 | 已迁移 | 总数 | 进度 |
|----------|--------|------|------|
| mk-* sections | 63 | ~210 | 30% |
| mk-* snippets | 148 | ~180+ | 82% |
| 图标资源 | 24 | ~30 | 80% |
| 翻译文件 | ✅ 完成 | - | 100% |

---

## ✅ 已完成的迁移

### MK-* Sections (67个)

**页面结构类 (8个)**
- [x] mk-main-collection.liquid - 产品集合页面
- [x] mk-main-product.liquid - 产品详情页面
- [x] mk-main-blog.liquid - 博客列表页面
- [x] mk-main-article.liquid - 文章详情页面
- [x] mk-main-account.liquid - 账户页面
- [x] mk-main-login.liquid - 登录注册页面
- [x] mk-404.liquid - 404错误页面
- [x] mk-page.liquid - 自定义页面

**导航类 (4个)**
- [x] mk-header.liquid - 顶部导航
- [x] mk-announcement-bar.liquid - 公告栏
- [x] mk-footer.liquid - 页脚
- [x] mk-mega-menu-desktop.liquid - 桌面端Mega菜单

**产品展示类 (8个)**
- [x] mk-product-card.liquid - 产品卡片
- [x] mk-product-overview.liquid - 产品概览
- [x] mk-product-specs.liquid - 产品规格
- [x] mk-featured-collection.liquid - 推荐产品集合
- [x] mk-card-banner.liquid - 卡片横幅
- [x] mk-media-grid.liquid - 媒体网格
- [x] mk-swiper-slider.liquid - 轮播滑块
- [x] mk-tabs.liquid - 标签页

**内容展示类 (10个)**
- [x] mk-hero-split.liquid - 分屏横幅
- [x] mk-image-banner.liquid - 图片横幅
- [x] mk-image-with-text.liquid - 图片配文本
- [x] mk-rich-text.liquid - 富文本
- [x] mk-blog-posts.liquid - 博客文章列表
- [x] mk-testimonials.liquid - 客户评价
- [x] mk-newsletter.liquid - 邮件订阅
- [x] mk-contact-form.liquid - 联系表单
- [x] mk-faq.liquid - 常见问题
- [x] mk-accordion-faq.liquid - 手风琴FAQ

**功能组件类 (10个)**
- [x] mk-countdown-timer.liquid - 倒计时
- [x] mk-feature-icon-grid.liquid - 图标网格
- [x] mk-icon-boxes.liquid - 图标盒子
- [x] mk-custom-content.liquid - 自定义内容
- [x] mk-logo-marquee.liquid - Logo滚动
- [x] mk-video-popup.liquid - 视频弹窗
- [x] mk-comparison-table.liquid - 比较表格
- [x] mk-cart.liquid - 购物车页面
- [x] mk-search.liquid - 搜索页面
- [x] mk-product-hotspots.liquid - 图片热点
- [x] mk-sticky-add-to-cart.liquid - 粘性购买按钮
- [x] mk-related-products.liquid - 相关产品
- [x] mk-trust-badges.liquid - 信任标识
- [x] mk-countdown-banner.liquid - 倒计时横幅
- [x] mk-promotion-banner.liquid - 促销横幅 (NEW)
- [x] mk-instagram-feed.liquid - Instagram动态 (NEW)
- [x] mk-image-gallery.liquid - 图片画廊 (NEW)
- [x] mk-video-section.liquid - 视频 (NEW)
- [x] mk-text-columns.liquid - 文本列 (NEW)
- [x] mk-rich-text.liquid - 富文本 (NEW)
- [x] mk-logo-list.liquid - Logo列表 (NEW)
- [x] mk-newsletter.liquid - 邮件订阅 (NEW)
- [x] mk-announcement-bar.liquid - 公告栏 (NEW)

### MK-* Snippets (33个)
- [x] mk-button.liquid - 按钮组件 (NEW)
- [x] mk-heading.liquid - 标题组件
- [x] mk-product-card.liquid - 产品卡片
- [x] mk-mega-menu-desktop.liquid - 桌面端Mega菜单
- [x] mk-mega-menu-desktop-image.liquid - 桌面端Mega菜单(图片版)
- [x] mk-mega-menu-mobile.liquid - 移动端Mega菜单
- [x] mk-icon.liquid - 图标组件
- [x] mk-cart-drawer.liquid - 购物车抽屉
- [x] mk-cart-products.liquid - 购物车商品列表
- [x] mk-cart-summary.liquid - 购物车汇总
- [x] mk-quick-add.liquid - 快速添加
- [x] mk-quick-add-modal.liquid - 快速添加模态框
- [x] mk-size-guide.liquid - 尺码指南
- [x] mk-stock-indicator.liquid - 库存指示器
- [x] mk-bento-grid.liquid - Bento网格 (NEW)
- [x] mk-contact-form.liquid - 联系表单 (NEW)
- [x] mk-price.liquid - 价格显示 (NEW)
- [x] mk-variant-picker.liquid - 变体选择器 (NEW)
- [x] mk-badge.liquid - 产品徽章 (NEW)
- [x] mk-rating.liquid - 评分组件 (NEW)
- [x] mk-share-button.liquid - 分享按钮 (NEW)
- [x] mk-quantity-selector.liquid - 数量选择器 (NEW)
- [x] mk-tabs.liquid - 标签页 (NEW)
- [x] mk-checkbox.liquid - 复选框 (NEW)
- [x] mk-divider.liquid - 分割线 (NEW)
- [x] mk-group.liquid - 群组块 (NEW)
- [x] mk-collection-card.liquid - 集合卡片 (NEW)
- [x] mk-card-gallery.liquid - 图片画廊卡片 (NEW)
- [x] mk-icon-or-image.liquid - 图标或图片 (NEW)
- [x] mk-image.liquid - 图片组件 (NEW)
- [x] mk-accordion.liquid - 手风琴 (NEW)
- [x] mk-pagination.liquid - 分页 (NEW)
- [x] mk-breadcrumbs.liquid - 面包屑 (NEW)

### 图标资源 (24个)
- [x] icon-account.svg - 账户图标
- [x] icon-arrow-left.svg - 左箭头
- [x] icon-arrow-right.svg - 右箭头
- [x] icon-cart.svg - 购物车图标
- [x] icon-check.svg - 勾选图标
- [x] icon-compare.svg - 比较图标
- [x] icon-facebook.svg - Facebook图标
- [x] icon-filter.svg - 筛选图标
- [x] icon-home.svg - 首页图标
- [x] icon-log-out.svg - 登出图标
- [x] icon-map-pin.svg - 位置图标
- [x] icon-menu.svg - 菜单图标
- [x] icon-package.svg - 包裹图标
- [x] icon-plus.svg - 加号图标
- [x] icon-return.svg - 退换图标
- [x] icon-search.svg - 搜索图标
- [x] icon-shield.svg - 安全图标
- [x] icon-truck.svg - 货车图标
- [x] icon-twitter.svg - Twitter图标
- [x] icon-user.svg - 用户图标
- [x] icon-wishlist.svg - 收藏图标

---

## 📋 待完成的迁移

### 优先级 P0 - 核心组件 (建议下一步)
- [ ] mk-cart-drawer.liquid - 购物车抽屉
- [ ] mk-quick-view.liquid - 快速查看
- [ ] mk-size-guide.liquid - 尺码指南
- [ ] mk-stock-indicator.liquid - 库存指示器

### 优先级 P1 - 重要组件
- [ ] mk-product-gallery.liquid - 产品画廊
- [ ] mk-sticky-add-to-cart.liquid - 粘性购买按钮
- [ ] mk-related-products.liquid - 相关产品
- [ ] mk-recently-viewed.liquid - 最近浏览
- [ ] mk-image-hotspots.liquid - 图片热点

### 优先级 P2 - 常用组件
- [ ] mk-promo-banner.liquid - 促销横幅
- [ ] mk-countdown-banner.liquid - 倒计时横幅
- [ ] mk Instagram-feed.liquid - Instagram动态
- [ ] mk-social-proof.liquid - 社交证明
- [ ] mk-trust-badges.liquid - 信任标识

### 优先级 P3 - 特殊功能
- [ ] mk-back-in-stock.liquid - 到货通知
- [ ] mk-product-bundle.liquid - 产品捆绑
- [ ] mk-gift-wrap.liquid - 礼品包装
- [ ] mk-store-locator.liquid - 店铺定位器

---

## 🔧 命名规范

### 文件前缀
- **mk-**: Monkey主题核心组件 (如 mk-header.liquid)
- **mk-**: Snippet组件 (如 mk-product-card.liquid)

### Schema命名
```json
{
  "name": "MK 组件名称",
  "tag": "section"
}
```

### 类名规范
```css
.mk-{component-name}
.mk-{component-name}__{element}
.mk-{component-name}--{modifier}
```

---

## 📁 目录结构

```
monkey/
├── sections/
│   ├── mk-*.liquid          # 核心组件
│   └── *.liquid              # 标准主题组件
├── snippets/
│   ├── mk-*.liquid           # 可复用组件
│   └── *.liquid              # 标准snippet
├── assets/
│   ├── *.css                 # 样式文件
│   ├── *.js                  # JavaScript文件
│   └── icon-*.svg            # 图标资源
├── layout/
│   └── theme.liquid          # 主题布局
├── templates/
│   └── *.json                # 页面模板
├── locales/
│   ├── en.default.json       # 英文字典
│   └── zh-CN.json            # 中文字典 ✅
└── config/
    └── settings_schema.json  # 设置模式
```

---

## 🌐 翻译文件状态

### ✅ 已完成
- **en.default.json**: 完整的英文翻译
- **zh-CN.json**: 完整的中文翻译 (4899 bytes)

### 翻译覆盖范围
- [x] 通用术语 (general)
- [x] 标签 (labels)
- [x] 选项 (options)
- [x] 产品 (products)
- [x] 博客 (blog)
- [x] 购物车 (cart)
- [x] 集合 (collections)
- [x] 搜索 (search)
- [x] 联系 (contact)
- [x] 订阅 (newsletter)
- [x] 客户 (customers)
- [x] 404 (404页面)
- [x] 礼品卡 (gift_card)
- [x] 密码 (password)
- [x] 组件名称 (sections.*)

---

## 📊 统计信息

- **创建时间**: 2026-04-11
- **最后更新**: 2026-04-13
- **总迁移文件**: ~90 个
- **总代码量**: ~700KB
- **完成度**: 约 45%

---

## 🔄 更新日志

### 2026-04-13 (第四次更新)
1. 新增 6个 mk-* sections (product-hotspots, sticky-add-to-cart, related-products, trust-badges, countdown-banner)
2. 新增 7个 mk-* snippets (cart-drawer, cart-products, cart-summary, quick-add, quick-add-modal, size-guide, stock-indicator)
3. 更新 MIGRATION_SPEC.md

### 2026-04-12 (第三次更新)
1. 完成 zh-CN.json 翻译文件
2. 新增 9个 mk-* 核心页面组件
3. 新增 20+ 图标资源
4. 更新 MIGRATION_SPEC.md

### 2026-04-12 (第二次更新)
1. 完成 17个 mk-* sections (mypetcustom项目)
2. 完成 6个 mk-* snippets
3. 完成 8+ MD文档

### 2026-04-11 (首次创建)
1. 分析三个源项目
2. 创建 MIGRATION_SPEC.md
3. 建立 monkey 主题基础结构
