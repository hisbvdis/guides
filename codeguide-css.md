# Стиль кода

## Последовательность классов
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
    font-style: normal;
    font-size: 14px;
    line-height: 24px;
    font-weight: 700;
    text-align: center;
    color: #ffffff;
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