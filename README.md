# Questions

1. Что такое React?
  JavaScript-библиотека для создания пользовательских интерфейсов. Создание одностраничного приложения.

2. Назовите основные особенности REACT?
- Использование virtualDOMd
- Поддержка рендеринга на стороне сервера
- Следование принципу однонаправленного потока и связывание данных
- Использование переиспользуемых компонентов пользовательского интерфейса

3. Что такое JSX?
   
   JSX – это синтаксическая обертка над JS.
   JSX позволяет нам писать HTML-синтаксис внутри JavaScript.
   JSX — это синтаксический сахар для функции React.createElement(), которая позволяет описывать структуру интерфейса приложения более наглядно и удобно.

const element = React.createElement(
  "h1",
  null,
  "Hello, world!"
); // без JSX

4. В чем разница между элементом и компонентом?
Элемент - это обычный объект, мы можем увидеть его в DOM дереве. Элементы могут содержать другие элементы в своих свойствах.
Компонент принимает свойства (пропы, props от properties) на вход и возвращает JSX, может быть функциональным или классовым.

5. Как в React создаются компоненты?
2 способа: 
1) Функциональные компоненты: это простейший способ создания компонента. Эти функции являются "чистыми", принимают объект с пропами в качестве аргумента и возвращают элемент(ы).
2) Классовые компоненты: для определения компонента также можно использовать ES6-классы. 

6. Когда лучше использовать классовый компонент, а когда функциональный?
   Если компонент нуждается в состоянии или методах жизненного циакла, тогда лучше использовать классовый компонент, иначе функциональный компонент.

7. Что такое "чистые" компоненты (Pure Components)?
Чистый компонент в React — это компонент, который всегда рендерит одно и то же при одних и тех же значениях пропсов.
- В React.PureComponent реализован метод жизненного цикла shouldComponentUpdate(), отвечающий за проверку, нужно ли производить перерисовку компонента или нет. Он производит поверхностное сравнение пропов и состояния компонента с предыдущими, чтобы понять, изменились ли они, и перерисовка происходит только в случае нахождения различий.
- В React.Component перерисовка происходит всегда, так как подобная проверка отсутствует. Однако при желании ее может реализовать программист.

 8. Что такое состояние (state) в React?

Состояние - это объект, содержащий некоторую информацию, которая может измениться в течение жизненного цикла компонента. Мы всегда должны стараться делать состояние настолько простым, насколько это возможно, и минимизировать количество компонентов без состояния.

9. Что такое пропы (props) в React?

Props - это входные данные для компонента. Это простые значения (примитивы) или объект, содержащий несколько значений, которые передаются компонентам при их создании с помощью синтаксиса, похожего на атрибуты HTML-тегов.

10. В чем разница между состоянием и пропами?

И props,  и state являются обычными JavaScript-объектами. Несмотря на то, что они оба содержат информацию, которая используется при рендеринге компонента, функционал у них разный. Пропы передаются компоненту подобно аргументам, передаваемым функции, а состояние управляется компонентом как переменные, объявленные внутри функции.

11. Что такое синтетические события в React?
SyntheticEvent - это кроссбраузерная оболочка для нативных событий браузера. Этот API аналогичен браузерному, включая stopPropagation() и preventDefault(), но работает одинаково во всех браузерах.

12.Что такое селектор CSS?

Селектор CSS — это шаблон элемента, который сообщает браузеру, какие элементы HTML он должен выбрать для применения значений свойств CSS. Поэтому, когда мне нужно выбрать какой-либо контент и применить к нему изменения, я могу использовать селектор CSS. Спецификация селекторов CSS определяет селекторы, и для работы селекторы должны поддерживаться браузером. Существует много типов селекторов CSS, таких как селектор классов CSS, универсальный селектор CSS, селектор идентификаторов CSS и селектор групп CSS

13. Какая разница между элементами div и span?

Div — блочный элемент, а span — строчный элемент. В соответствии с семантическими требованиями div используют для группировки контента в секции, а span — для оформления текста и изображений.

14. Расскажите о блочной модели CSS

Блочная модель CSS – это прямоугольное пространство вокруг элемента HTML, в котором определяются границы, поля и отступы.
- Границы – определяют максимальную область, в которой будет содержаться элемент. Мы можем сделать границу видимой, невидимой, определить высоту и ширину элемента и т.п. -
- Поля – определяют расстояния между границами и элементом.
- Отступы – определяют расстояния между границами и соседними элементами.

15. Объясните делегирование событий
    
Делегирование событий - это приём, заключающийся в добавлении обработчиков событий к родительскому элементу, а не к дочерним элементам. Обработчик будет срабатывать всякий раз, когда событие будет запущено на дочерних элементах благодаря всплытию событий в DOM. Преимущества этого приёма:

Экономит объем используемой памяти, т.к. для родительского элемента требуется только один обработчик.
Не нужно привязывать или убирать обработчики при добавлении и удалении элементов.

16. ЧТО ТАКОЕ HTML-ЭЛЕМЕНТ? КАКОВА ЕГО СТРУКТУРА?
Элемент HTML — основная структурная единица веб-страницы, написанная на языке HTML.
•	Тег HTML — указывает браузеру, как контент должен отображаться в нем.
•	Любой HTML-документ состоит из трех частей — определение типа документа, голова и тело.
•	HTML 5 определяется с помощью <!DOCTYPE html>, в то время как HTML 4 имеет три разных способа определения типа — Strict, Transitional и фреймовая структура HTML.
•	<html> — это корневой элемент, который не может помещаться в любой другой.
•	Элементы <head> и <body> вкладываются внутрь элемента <html>.
•	<head> содержит информацию для браузера
•	<body> содержит все, что должно быть отображено в окне браузера.
•	Элемент HTML — это комбинация открывающего тега, содержимого и закрывающего тега.
•	Декларация Doctype сообщает браузеру, какому стандарту он следует.
•	<head> может содержать заголовок, таблицы стилей, скрипты и метаданные.
•	Метаданные — это информация о документе, но не его содержимое.


