1) как вызвать сетку
Для вызова сетки нужно сообщить параметр grid для основного класса.
Наберем код в файле (index.html или верхняя часть онлайн редактора):
<div class="parent">
  <div class="child">Привет, </div>
  <div class="child1"> мир</div>
</div>

2) как сделать таблицу 2х3
  Для работы понадобится редактор https://html-css-js.com

Наберем код в файле (index.html или верхняя часть онлайн редактора https://html-css-js.com):
<div class="grid-init grid">
    <div class="box-init box">A</div>
    <div class="box-init box">B</div>
    <div class="box-init box">C</div>
    <div class="box-init box">D</div>
    <div class="box-init box">E</div>
    <div class="box-init box">F</div>
</div>


/* CSS styles */

* {
    /*  width и height элементов включают в
        себя значения полей и границ  */
    box-sizing: border-box;
}
.grid-init {
    max-width: 400px; /* максимальная ширина контейнера */
    margin: auto; /* центрирование контейнера на странице */
    background-color: lightsteelblue; /* фон */
    padding: 10px; /* внутренние отступы */
}
.box-init {
    font-size: larger; /* размер шрифта */
    color: #fff; /* цвет текста */
    border-radius: 5px; /* скругление углов */
    background-color: #2196f3; /* цвет фона */
    border: 1px solid black; /* граница блока */
    padding: 10px; /* внутренние отступы */
    /*  выравнивание текста по центру блока
        с помощью CSS Flexbox  */
    display: flex;
    align-items: center;
    justify-content: center;
}
.grid {
    display: grid; /*вызвали сетку*/
  grid-gap: 10px; column-gap: 10px;
  grid-template-columns: 1fr 1fr;/* создали колонки одинаковой ширины*/
  grid-template-rows: 1fr 1fr 1fr ;/* создали строки одинаковой ширины*/


3) при помощи чего задается очередность вывода ячеек
   По умолчанию все элементы располагаются по порядку горизонтально, если места в строке больше нет, то элементы переносятся на следующую строку. Но с помощью свойства grid-auto-flow можно изменить направление элементов. Это свойство принимает два значения:
row: значение по умолчанию, элементы располагаются в строку друг за другом, если места в строке не хватает, элементы переносятся на следующую строку
column: элементы располагаются в столбик, если места в столбце не хватает, то элементы переходят в следующий столбец (см. задание 2)
Свойство grid-auto-flow имеет значение row, поэтому элементы будут располагаться в строку. 

В Grid Layout мы можем дать наименование каждой линии грида, присвоив ей какое-либо имя в квадратных скобках и затем, используя это имя, позиционировать элементы. 

Также можно описать каждую ячейку, присвоив ей индивидуальное имя, которое можно в последствии использовать в раскладке (очередности и месте элементов) шаблона сайта.


Создадим структуру сайта в файле (index.html или верхняя часть онлайн редактора https://html-css-js.com):

<div class="grid-init grid">
    <header class="box-init box l-header">HEADER</header>
    <nav class="box-init box l-nav">NAV</nav>
    <main class="box-init box l-main">MAIN</main>
    <aside class="box-init box l-aside">ASIDE</aside>
    <section class="box-init box l-section">SECTION</section>
    <footer class="box-init box l-footer">FOOTER</footer>
</div>
