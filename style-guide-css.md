# Стиль кода - CSS

## Названия переменных
**Обычные названия**<br/>
Для белого, чёрного и других конкретных цветов указывать название прямо в переменной
```css
  --color-white: #fff;
  --color-black: #000;
```
**Яркость цвета**<br/>
Если цвет имеет много оттенков, задавать их градацию с помощью ключевых слов яркости
```css
  --color-red-lightest: #fff;
  --color-red-lighter: #fff;
  --color-red-light: #fff;
  --color-red-regular: #fff;
  --color-red-dark: #fff;
  --color-red-darker: #fff;
  --color-red-darkest: #fff;
```
**Брендовый цвет**<br/>
Для "фирменного" цвета можно выделить "брендовую" переменную
```css
  --color-brand: #fff;
```

**Размер шрифта**<br/>
Можно указывать фиксированный размер шрифта или диапазон размеров, если он отзывчивый
--fontSize-12: 12rem;
--fontSize-12-18: clamp(var(--fontSize-12), 3vw, var(--fontSize-18));

**Другие названия**<br/>
```css
  --color-accent: #fff;
```

**Примеры названий**
- Градиент: 
  ```css 
  --bg-gradient: linear-gradient(to right, #fff, #000);
  ```
- Тень:
  ```css
  --shadow-bg: 0 0 20px rgb(0 0 0 / 0.1);
  ```
- Радиус скругления углов:
  ```css
  --borderRadius-10px: 10px;
  ```
- Семейство шрифтов:
  ```css
  --fontFamily-1: "Montserrat";
  ```

## Последовательность свойств
```css
.selector {
    /* Позиционирование */
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 100;

    /* Блочная модель (размеры и отступы) */
    display: block;
    float: right;
    width: 100px;
    height: 100px;
    margin: 40px;
    padding: 20px;

    /* Текст */
    font-family: Arial, Helvetica, sans-serif;
    font-size: 14px;
    line-height: 24px;
    font-weight: 700;
    color: #ffffff;
    font-style: normal;
    text-align: center;
    text-transform: uppercase;

    /* Оформление (визуализация) */
    background-color: #f5f5f5;
    border: 1px solid #e5e5e5;
    border-radius: 3px;
    opacity: 1;

    /* Переходы, анимация */
    transition: all 1s;
    animation: anime 1s infinite;

    /* Другое */
    will-change: auto;}
```

## Порядок атрибутов
- class
- id, name
- data-*
- src, for, type, href, value
- title, alt
- role, aria-...