# Практическая работа 2

Адаптивный каталог на HTML и SCSS.

## Запуск

Открыть `index.html` в браузере.

Сборка SCSS (нужен Node.js):

```
npx sass scss/styles.scss css/styles.css --no-source-map
```

Наблюдение за изменениями:

```
npx sass --watch scss/styles.scss css/styles.css --no-source-map
```

## Dataset

- `catalog.csv` — 12 карточек
- `theme.json` — цвета, радиус и отступ в `_variables.scss`
- `product-01/02/03.svg` — картинки товаров

## SCSS

- Шаг 8: вложенность `.header a`, `.card h3`, `.button:hover`
- Шаг 9: mixin `box` в `.card`, `.filters`, `.info`
- Шаг 10: функция `space(2)` = 32px
- Шаг 12: 3 колонки, на планшете 2, на телефоне 1
- Шаг 13: на 768px фильтры над каталогом, на 480px одна колонка

SCSS-переменная `$accent` есть только при сборке, в CSS вместо неё стоит значение. CSS-переменная `--accent` остаётся в CSS, и браузер может её менять.

Partial-файлы (с `_`) не собираются сами, а подключаются в `styles.scss` через `@use`.
