# sass-landing-page-refactor

Tái cấu trúc mã CSS của Landing Page (navigation + header, sản phẩm nổi bật, số liệu thống kê, footer) sang SASS/SCSS.

## Tính năng SASS đã áp dụng

- **Variables**: màu sắc, font, kích thước container, transition, shadow, breakpoint (`abstracts/_variables.scss`).
- **Mixins**: `flex-center`, `mobile` (media query với `@content`), `card-surface` (`abstracts/_mixins.scss`).
- **Nesting**: lồng selector, `&:hover`, `&-primary`, `&__content` (BEM).
- **Hàm màu**: `rgba($color, alpha)`, `color.adjust($color, $lightness: -3%)` (module `sass:color`).
- **Partials** chia theo `abstracts`, `base`, `components`, `layout`, gộp trong `style.scss`.

## Cấu trúc thư mục

```
sass-landing-page-refactor/
├── scss/
│   ├── abstracts/
│   │   ├── _variables.scss
│   │   └── _mixins.scss
│   ├── base/
│   │   └── _reset.scss
│   ├── components/
│   │   ├── _buttons.scss
│   │   └── _cards.scss
│   ├── layout/
│   │   ├── _header.scss
│   │   ├── _features.scss
│   │   ├── _stats.scss
│   │   └── _footer.scss
│   └── style.scss
├── css/
│   └── style.css        # CSS biên dịch
├── index.html
└── package.json
```

## Biên dịch

```bash
npm install
npm run build   # scss/style.scss -> css/style.css
npm run watch   # tự động biên dịch khi lưu file
```

Sau đó mở `index.html` trong trình duyệt.
