# Методические указания по созданию дизайна в Figma и верстке

<!-- ## План

1. [Начало работы с Figma](#начало работы с Figma)
2. [Создание карточки](#создание карточки)
3. [Страница подробного описания](#cтраница подробного описания)
4. HTML и CSS
5. Верстка карточки
6. Верстка страницы карточек
7. Верстка подробного описания


## Немного про SwiftUI
SwiftUI - это фреймворк для создания пользовательских интерфейсов на языке программирования Swift. Он был представлен Apple на -->

## Начало работы с Figma

Figma (Фигма) — это графический онлайн-редактор для совместной работы. Figma используют в основном для создания прототипов сайтов и приложений.
С фигмой можно работать с помощью [сайта](https://www.figma.com/) и [десктопного приложения](https://www.figma.com/downloads/) (после нажатия на "Desktop app for macOS" или "Desktop app for Windows"). Далее необходимо войти в аккаунт или зарегистрироваться.

После авторизации открывается главная страница, на которой в центре отображаются проекты, слева панель для перехода к недавним проектам, черновикам, избранными и проектами комманд (можно создавать команды и вместе создавать и работать над общими проектами).
![Alt text](assets/главная.png)

Для создания проекта на левой панели нажимаем Drafts, затем на верхней панели Design file
Интерфейс можно разделить на 4 области:
1. Слева - слои
2. В центре - рабочее пространство
3. Справа - редактирование свойств объектов
4. Сверху - инструменты 
![Alt text](assets/проект.png)

## Создание страницы карточек
Создаем фрейм — основной элемент дизайна в Фигме. Это законченный документ, который может быть страницей сайта или экраном мобильного приложения. Фрейм объединяет объекты внутри себя.

![Alt video](assets/frame.gif)

Добавим странице цвет, нажимаем на фрейм, в правой панели находим вкладку Fill - она отвечает за заливку, нажимаем на квадратик. Ползунок позволяет выбрать цвет или можно ввести код цвета.

![Alt text](assets/color.png)

Остальные элементы добавим потом

## Создание карточки
Карточка будет отображать картинку, название, краткое описание, цену и кнопку для перехода к странице подробного описания продукта.
Необходимы - 2 прямоугольника, картинка, 3 текстовых блока.

Для создания прмоугольника надо выбрать его в панеле инструментов или нажать клавишу R, в рабочей области удерживая левую кнопку мыши создать прямоугольник произвольного размера.
Во вкладке с прямоугольником можно выбрать линию, стрелку, эллипс, многоугольник, звезду и изображение

![Alt video](assets/квадрат.gif)
Создадим еще один прямоугольник, добавим изображение и текстовые элементы. Когда мы создаем внутри фрейма элементы, они автоматически в панели слоев создаются внтури этого фрейма
![Alt text](assets/элементы.png)

### Свойства элементов
Свойства элементов настраиваются в правой панели

Свойства текста:
1. Шрифт. Выбрать шрифт можно на сайтее [Google Fonts](https://fonts.google.com/). Нажимаем на Filters->Language. Выбираем Cyrillic, чтоб выбрать шрифт, поддерживающий русский язык.
![Alt text](assets/выбор%20шрифта.png)
2. Стиль - у краткого описания и кнопки пусть будет Medium, у названия и цены - SemiBold
3. Размер - на сайтах для обычного текста имеют размер 14px, сделаем для краткого описания и кнопки так же, а название и цену размера 16px, чтоб они выделялись

Выбираем текстовый элемент, во вкладке Text нажимаем на название шрифта, находим необходимый шрифт, ниже устанавливаем стиль и размер шрифта. Если нажать на три точки, то откроется со всеми настройками шрифта
![Alt text](assets/шрифт.png)

Аналогично сделаем для других текстовых элементов.
![Alt text](assets/элементы.png)

Свойства геометрических элементов:
1. Цвет. Это уже умеем делать
2. Скругление углов.
Рассмотрим параметры этой вкладки: X, Y - координаты элемента внтури фрейма, W, H - ширина и высота, пиктограмма угла - угол поворота элемента, скругление углов
Сделаем скругление у карточки и изображения 20px, а у кнопки 10px
![Alt text](assets/скругление.png)
3. Обводка. У кнопки сделаем обводку, а заливку уберем.
Для этого в Stroke нажмем на "+", добавится обводка. У нее можно настроить цвет, толщину, стороны, для которых их добавить. В Fill нажмем на "-" у цвета

Свойства изображения:
Для изменения размера нужно потянуть за границы изображения, при этом для пропорционального изменения сторон необходимо зажимать Shift.
Если вам необходимо обрезать картинку, перейдите во вкладку Fill и нажмите на изображение. В открывшемся окне над изображением есть выпадающий список, в нем надо выбрать Crop и менять границы. Если вы хотите заменить картинку, наведите на картинку в этом окне, появится кнопка "Choose image"
![Alt text](assets/обрезка.png)

### Компановка карточки и Auto Layout
Мы подготовили все элементы, теперь скомпануем их.
Для начала сгруппируем кнопку. Выбираем с нажатой клавишей Shift прямоугольник и текст для кнопки, в правой панели в самой первой вкладке можно настраивать выравнивание, нам надо выровнять элементы относительно друг друга по вертикали и горизонтали, нажимаем на 2 и 5 значки, затем нажмите Ctrl+G (группировка элементов)

![Alt video](assets/кнопка.mp4)

Теперь собираем карточку, переносим элементы на прямоугольник, являющийся фоном карточки, выравниваем элементы, располагаем цену и кнопку на одном уровне и группируем. Если несколько элементов сгруппированы, то при одном клике на элемент, будет выделена вся группа, поэтому надо два раза кликнуть по элементу, чтоб выделить именно его.

В фигме есть такой инструмент, как Auto Layout. Это позволяет создавать контейнеры, которые могут содержать другие элементы интерфейса, затем можно настроить правила расположения, такие как выравнивание или расстояние между элементами. Auto layout можно сравнить с flex в css.
Выделяем все элементы карточки, включая ее фон, в правой панели находим вкладку Auto layout, нажимаем плюс.

![Alt text](assets/auto%20layout.png)
Выбираем вертикально расположение, внутренний отступ (padding) 20px, интервал между элементами 10px. 
Копируем карточку, меняем содержимое.
Итог:
![Alt text](assets/все%20карточки.png)


## Страница подробного описания

Сделаем картинку и описание на отдельных блоках

## HTML и CSS

HTML - язык разметки гипертекста. Включает теги
С помощью html мы создаем элементы, а с помощью css - задаем им свойства

CSS - 

## Верстка страницы с карточками

<img src="assets/главная.jpg" height="300px">

Сначала создадим разметку, а потом будем прописывать свойства
Создаем файл index.html и style.css, в index.html пишем

```html
<!DOCTYPE html>
<!-- {% load static %} -->
<html lang="rus">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Магазин</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="space">
        <div class="header"></div>
        <div class="container"></div>
    </div>
  </body>
</html>
```
<!-- надо добавить описание каждой строки -->
Внутри body создадим div с именем space, внутри которого будем располагать наши элементы
Страница разделена на две части: хедер и контейнер
В хедере будет название компании, навигационная панель
В контейнере будут карточки

Файл style.css
```css
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat', sans-serif;
    color: #000000; 
}
body{
    background: #EFEFEF;
}
.space{
    width: 80%;
    margin-left: auto;
    margin-right: auto;
}
```

На [сайте]() выбираете понравившийся Cyrrylic шрифт 
<!-- ну и что-то еще -->
Копируем import 

background - цвет фона элементы 
width - ширина
margin-left - расстояние слева
margin-right - расстояние справа

Единицы измерения в css
<!-- добавить -->

## Верстка карточки

Добавим это внутрь класса container
```html
<div class="card">
    <img src="./img/1.jpg" class="image">
    <p class="title">LA ROCHE-POSAY effaclar</p>
    <p class="short-description">Крем-гель для проблемной кожи</p>
    <p>1348 ₽</p>
    <a href="./detail.html" class="card-button">Подробнее</a>
</div>
```
<!-- описание карточки -->

Сделаем карточку красивой

```css
.card{
    border-radius: 20px;
    background: #FFFAFA;
    padding: 10%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
```
border-radius - скругление
display - 
flex-direction: column - расположение элементов в столбик внутри блока 
justify-content - расположение элементов относительно друг друга

Стили для картинки
```css
.image{
    width: 100%;
    height: 211px;
    border-radius: 20px;
    object-fit: cover;
}
```
Картинка будет занимать 100% доступной ей ширины, так как у карточки padding - 10%, то картника будет заполнять в ширину 80% карточки и располагаться по центру

Посмотрим высоту картчоки и скругление в фигме
<!-- картинка из фигмы -->
object-fit: cover - 

```css
.title{
    margin-top: 15px;
    font-size: 16px;
    font-weight: bold;
}
```

```html
<div class="card">
    <div class="info">
        <img src="./img/2.jpg" class="image">
        <p class="title">LA ROCHE-POSAY nutritic intense riche</p>
        <p class="short-description">Питательный крем для глубокого восстановления сухой кожи</p>
    </div>
    <div class="down">
        <p>1915 ₽</p>
        <a href="" class="card-button">Подробнее</a>
    </div>
</div>
```

## Верстка подробного описания


