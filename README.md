# Cheatsheet 2.0

Шпаргалка по созданию сайтов с помощью HTML и CSS.

Здесь собраны основные теги HTML и самые нужные свойства CSS — всё в одном месте, чтобы быстро вспоминать синтаксис и собирать страницу без лишнего поиска.

## Как пользоваться

1. Найди, что хочешь сделать.
2. Посмотри нужный тег или CSS-свойство.
3. Вставь его в свой код.

## HTML

### Структура страницы

| Тег | Что делает | Где использовать |
|---|---|---|
| `<!DOCTYPE html>` | Объявляет HTML5 | В самом начале файла |
| `<html>` | Корневой тег страницы | После `DOCTYPE` |
| `<head>` | Служебная информация | Внутри `<html>` |
| `<title>` | Название страницы | Внутри `<head>` |
| `<meta charset="UTF-8">` | Поддержка русских букв | Внутри `<head>` |
| `<meta name="viewport">` | Адаптивность на мобильных | Внутри `<head>` |
| `<link>` | Подключение CSS-файла | Внутри `<head>` |
| `<style>` | Встроенные CSS-стили | Внутри `<head>` или `<body>` |
| `<body>` | Весь видимый контент | После `<head>` |

### Блоки и контейнеры

| Тег | Что делает | Когда использовать |
|---|---|---|
| `<header>` | Шапка сайта | Логотип, меню, контакты |
| `<main>` | Основной контент | Главная информация страницы |
| `<section>` | Смысловой блок | Разделы вроде «О нас» или «Услуги» |
| `<footer>` | Подвал сайта | Копирайт, ссылки, контакты |
| `<div>` | Универсальный контейнер | Для группировки любых элементов |
| `<span>` | Строчный контейнер | Для части текста внутри строки |

### Текст

| Тег | Что делает |
|---|---|
| `<h1>` | Главный заголовок страницы |
| `<h2>` | Заголовок раздела |
| `<h3>`–`<h6>` | Подзаголовки |
| `<p>` | Абзац текста |
| `<br>` | Перенос строки |
| `<hr>` | Горизонтальная линия |

### Ссылки и кнопки

| Тег | Что делает | Атрибуты |
|---|---|---|
| `<a>` | Ссылка | `href="url"` |
| `<button>` | Кнопка | `type="button"` |

### Медиа

| Тег | Что делает | Атрибуты |
|---|---|---|
| `<img>` | Изображение | `src`, `alt` |
| `<video>` | Видео | `src`, `controls` |
| `<audio>` | Аудио | `src`, `controls` |

### Списки

| Тег | Что делает |
|---|---|
| `<ul>` | Маркированный список |
| `<ol>` | Нумерованный список |
| `<li>` | Элемент списка |

### Таблицы

| Тег | Что делает |
|---|---|
| `<table>` | Таблица |
| `<tr>` | Строка |
| `<td>` | Ячейка |
| `<th>` | Заголовочная ячейка |

### Формы

| Тег | Что делает |
|---|---|
| `<form>` | Контейнер формы |
| `<input>` | Поле ввода |
| `<textarea>` | Большое текстовое поле |
| `<label>` | Подпись к полю |

## CSS

### Селекторы

| Селектор | Пример | Что выбирает |
|---|---|---|
| Тег | `h1 {}` | Все `<h1>` |
| Класс | `.card {}` | Элементы с `class="card"` |
| ID | `#logo {}` | Элемент с `id="logo"` |
| Все элементы | `* {}` | Всё на странице |

### Цвета и фон

```css
color: red;
color: #ff0000;
color: rgb(255, 0, 0);

background: white;
background: #f0f0f0;
background: linear-gradient(135deg, #667eea, #764ba2);
background-image: url('bg.jpg');

opacity: 0.5;
```

### Размеры

```css
width: 300px;
width: 100%;
width: 50vw;
max-width: 1200px;
min-width: 200px;
height: auto;
height: 100vh;
```

### Отступы

```css
padding: 20px;
padding: 10px 20px;
padding-top: 10px;
padding-bottom: 10px;
padding-left: 20px;
padding-right: 20px;

margin: 20px;
margin: 0 auto;
margin-top: 10px;
margin-bottom: 10px;
```

### Рамки и тени

```css
border: 2px solid black;
border: 2px dotted red;
border: 2px dashed blue;
border: none;

border-radius: 10px;
border-radius: 50%;
border-radius: 10px 20px;

box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.2);
text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
```

### Текст и шрифты

```css
text-align: left;
text-align: center;
text-align: right;

line-height: 1.5;
vertical-align: middle;

font-family: Arial, sans-serif;
font-size: 16px;
font-weight: bold;
font-style: italic;
text-decoration: none;
text-decoration: underline;
```

### Отображение

```css
display: block;
display: inline;
display: inline-block;
display: none;
display: flex;
display: grid;
```

### Flex

```css
.parent {
    display: flex;
    gap: 20px;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}

.child {
    flex: 1;
}
```

### Grid

```css
.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}
```

### Hover и анимация

```css
.button:hover {
    background: darkred;
    transform: scale(1.05);
    transform: rotate(10deg);
    transition: 0.3s;
}
```

### Адаптивность

```css
@media (max-width: 768px) {
    .container {
        flex-direction: column;
    }

    .card {
        width: 100%;
    }
}
```

### Полезные мелочи

```css
ul {
    list-style: none;
}

button {
    cursor: pointer;
}

* {
    transition: all 0.2s ease;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

## Пример


```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мой сайт</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: system-ui, sans-serif;
            background: white;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            background: #333;
            color: white;
            padding: 20px 0;
        }

        .flex-row {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            margin: 40px 0;
        }

        .card {
            flex: 1;
            min-width: 250px;
            background: #f0f0f0;
            padding: 20px;
            border-radius: 16px;
            text-align: center;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            transition: 0.3s;
        }

        .btn {
            display: inline-block;
            background: #007bff;
            color: white;
            padding: 12px 24px;
            text-decoration: none;
            border-radius: 30px;
            margin-top: 20px;
        }

        .btn:hover {
            background: #0056b3;
        }

        h1 {
            font-size: 48px;
            text-align: center;
            margin: 40px 0;
        }

        h2 {
            font-size: 32px;
            margin: 30px 0 20px;
        }

        .footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 40px;
            margin-top: 60px;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 32px;
            }

            h2 {
                font-size: 24px;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="container">
            <h2>Мой логотип</h2>
        </div>
    </div>

    <div class="container">
        <h1>Привет, я делаю сайт</h1>

        <div class="flex-row">
            <div class="card">
                <h3>Услуга 1</h3>
                <p>Описание первой услуги</p>
                <a href="#" class="btn">Подробнее</a>
            </div>

            <div class="card">
                <h3>Услуга 2</h3>
                <p>Описание второй услуги</p>
                <a href="#" class="btn">Подробнее</a>
            </div>

            <div class="card">
                <h3>Услуга 3</h3>
                <p>Описание третьей услуги</p>
                <a href="#" class="btn">Подробнее</a>
            </div>
        </div>

        <hr>

        <h2>О нас</h2>
        <p>Здесь можно написать описание компании или проекта.</p>

        <img src="photo.jpg" alt="Картинка" style="width: 100%; border-radius: 16px; margin: 20px 0;">
    </div>

    <div class="footer">
        <p>© 2025 Мой сайт. Все права защищены.</p>
        <p>email@example.com | +7 999 123-45-67</p>
    </div>
</body>
</html>
```
