# Cheetsheet2.0
Шпаргалка по созданию сайта 
📘 Полный справочник тегов HTML и свойств CSS (для любого сайта)

Как пользоваться: ищешь что хочешь сделать → смотришь тег/свойство → ставишь в нужное место

---

ЧАСТЬ 1: HTML — все теги, которые нужны

🏗️ Структура страницы (скелет)

Тег Что делает Куда ставить
<!DOCTYPE html> Говорит браузеру, что это HTML5 В самом начале файла
<html> Корневой тег, внутри вся страница После DOCTYPE
<head> Служебная информация (не видна на странице) Внутри <html> в начале
<title> Название страницы (на вкладке браузера) Внутри <head>
<meta charset="UTF-8"> Поддержка русских букв Внутри <head>
<meta name="viewport"> Адаптив на телефонах Внутри <head>
<link> Подключить CSS файл Внутри <head>
<style> Написать CSS прямо в HTML Внутри <head> или в <body>
<body> Всё, что видит пользователь После <head>

📦 Блоки и контейнеры

Тег Что делает Когда использовать
<header> Шапка сайта Логотип, меню, контакты вверху
<main> Главное содержание Всю основную информацию сюда
<section> Смысловой блок «О нас», «Услуги», «Контакты»
<footer> Подвал Копирайт, ссылки внизу
<div> Универсальный контейнер Группировка любых элементов
<span> Строчный контейнер Выделить часть текста внутри строки

📝 Текстовые теги

Тег Что делает Где юзать
<h1> Главный заголовок (один на странице) В начале <main>
<h2> Заголовок секции Внутри <section>
<h3>–<h6> Заголовки поменьше Для подзаголовков
<p> Абзац текста Для обычного текста
<br> Перенос строки Внутри <p> или где нужно
<hr> Горизонтальная линия Разделение блоков

🔗 Ссылки и кнопки

Тег Что делает Атрибуты
<a> Ссылка href="url" — куда ведёт
<button> Кнопка type="button"

🖼️ Медиа

Тег Что делает Атрибуты
<img> Картинка src="путь" — файл, alt="описание"
<video> Видео src, controls
<audio> Аудио src, controls

📋 Списки

Тег Что делает
<ul> Маркированный список (точки)
<ol> Нумерованный список (1,2,3)
<li> Один пункт списка (внутри ul/ol)

📊 Таблицы

Тег Что делает
<table> Создать таблицу
<tr> Строка таблицы
<td> Ячейка таблицы
<th> Заголовочная ячейка (жирный текст)

📝 Формы (если спросят)

Тег Что делает
<form> Контейнер для формы
<input> Поле ввода (текст, почта, пароль)
<textarea> Большое поле для текста
<label> Подпись к полю

---

ЧАСТЬ 2: CSS — все свойства для красоты

В CSS ты сначала выбираешь кому (тег, класс, id), потом пишешь что сделать (свойство: значение)

🎨 Как выбрать элемент (селекторы)

Селектор Пример Применяется к
Тег h1 { } Всем <h1>
Класс .card { } Всем с class="card"
ID #logo { } Элементу с id="logo"
Все элементы * { } Всему на странице

🌈 Цвета и фон

```css
/* Цвет текста */
color: red;
color: #ff0000;      /* HEX код */
color: rgb(255,0,0); /* RGB */

/* Фон */
background: white;
background: #f0f0f0;
background: linear-gradient(135deg, #667eea, #764ba2); /* градиент */
background-image: url('bg.jpg'); /* картинка на фон */

/* Прозрачность */
opacity: 0.5;        /* 0 — невидим, 1 — полностью видим */
```

📐 Размеры

```css
/* Ширина и высота */
width: 300px;
width: 100%;         /* на всю ширину родителя */
width: 50vw;         /* 50% ширины экрана */
max-width: 1200px;   /* не больше */
min-width: 200px;    /* не меньше */
height: auto;        /* автоматически */
height: 100vh;       /* на всю высоту экрана */
```

📍 Отступы (воздух вокруг)

```css
/* Внутренние (от края элемента до контента) */
padding: 20px;              /* со всех сторон */
padding: 10px 20px;         /* сверху/снизу 10, слева/справа 20 */
padding-top: 10px;
padding-bottom: 10px;
padding-left: 20px;
padding-right: 20px;

/* Внешние (между элементами) */
margin: 20px;
margin: 0 auto;             /* центрирование */
margin-top: 10px;
margin-bottom: 10px;
```

🖼️ Рамки и границы

```css
/* Обычная рамка */
border: 2px solid black;     /* сплошная */
border: 2px dotted red;      /* пунктир точками */
border: 2px dashed blue;     /* пунктир чёрточками */
border: none;                /* убрать рамку */

/* Скругление углов */
border-radius: 10px;         /* все углы */
border-radius: 50%;          /* круг */
border-radius: 10px 20px;    /* разные углы */

/* Тень */
box-shadow: 5px 5px 10px rgba(0,0,0,0.2);
text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
```

📍 Расположение (самое важное!)

Текст:

```css
text-align: left;      /* по левому краю */
text-align: center;    /* по центру */
text-align: right;     /* по правому краю */

/* Вертикальное выравнивание (для строк) */
line-height: 1.5;      /* межстрочный интервал */
vertical-align: middle;
```

Шрифты:

```css
font-family: Arial, sans-serif;
font-size: 16px;
font-weight: bold;     /* жирный */
font-weight: normal;
font-style: italic;    /* курсив */
text-decoration: none; /* убрать подчёркивание ссылки */
text-decoration: underline;
```

Отображение (как ведёт себя элемент):

```css
display: block;        /* на всю ширину, перенос строки */
display: inline;       /* в строку, не переносит */
display: inline-block; /* как inline, но можно задать ширину */
display: none;         /* скрыть элемент */

/* ✨ СВЕТАЯ ТРОИЦА ДЛЯ МАКЕТОВ ✨ */
display: flex;         /* гибкий контейнер (делим на части) */
display: grid;         /* сетка (таблица) */
```

🔥 FLEX (делим блок на части) — тебе это точно нужно

Ставишь на родителя:

```css
.parent {
    display: flex;
    gap: 20px;           /* расстояние между детьми */
    justify-content: center; /* по горизонтали: center, space-between, flex-start */
    align-items: center;     /* по вертикали: center, stretch */
    flex-wrap: wrap;         /* перенос на новую строку */
}
```

Ставишь на детей:

```css
.child {
    flex: 1;             /* растягиваются одинаково */
    flex: 2;             /* этот в 2 раза шире остальных */
}
```

🧱 GRID (сетка для карточек и галерей)

```css
.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);  /* 3 одинаковые колонки */
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* адаптив */
    gap: 20px;
}
```

🖱️ Эффекты при наведении

```css
.button:hover {
    background: darkred;
    transform: scale(1.05);  /* увеличить */
    transform: rotate(10deg); /* повернуть */
    transition: 0.3s;        /* плавность */
}
```

📱 Адаптив (под телефон)

```css
/* Когда экран уже 768px */
@media (max-width: 768px) {
    .container {
        flex-direction: column;  /* блоки встают в столбик */
    }
    .card {
        width: 100%;             /* карточки на всю ширину */
    }
}
```

🔧 Полезные мелочи

```css
/* Убираем маркеры списка */
ul {
    list-style: none;
}

/* Курсор при наведении */
button {
    cursor: pointer;
}

/* Плавные изменения */
* {
    transition: all 0.2s ease;
}

/* Сброс стилей по умолчанию (пиши в начале) */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

---

ЧАСТЬ 3: Как собрать всё вместе

Полный рабочий пример (копируй и меняй)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мой крутой сайт</title>
    <style>
        /* СБРОС */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: system-ui, sans-serif;
            background: white;
        }
        
        /* КОНТЕЙНЕР (узкий по центру) */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* ШАПКА */
        .header {
            background: #333;
            color: white;
            padding: 20px 0;
        }
        
        /* FLEX для карточек */
        .flex-row {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            margin: 40px 0;
        }
        
        /* КАРТОЧКА */
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
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            transition: 0.3s;
        }
        
        /* КНОПКА */
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
        
        /* ЗАГОЛОВКИ */
        h1 {
            font-size: 48px;
            text-align: center;
            margin: 40px 0;
        }
        
        h2 {
            font-size: 32px;
            margin: 30px 0 20px;
        }
        
        /* ПОДВАЛ */
        .footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 40px;
            margin-top: 60px;
        }
        
        /* АДАПТИВ */
        @media (max-width: 768px) {
            h1 { font-size: 32px; }
            h2 { font-size: 24px; }
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="container">
            <h2>Мой Логотип</h2>
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
        <p>Какой-то текст про компанию. Здесь можно написать что угодно.</p>
        
        <img src="photo.jpg" alt="Картинка" style="width: 100%; border-radius: 16px; margin: 20px 0;">
    </div>
    
    <div class="footer">
        <p>© 2025 Мой сайт. Все права защищены.</p>
        <p>email@example.com | +7 999 123-45-67</p>
    </div>
</body>
</html>
```
