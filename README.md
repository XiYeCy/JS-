# JS-getComputedStyle()；

今天在学习的过程中，遇到无法获取css里伪元素的问题。

经过上网查找，发现事情比我想象的麻烦。伪元素并不是DOM元素，无法被js直接操作。

通过查询我发现了一种方法，可以获取伪元素的css属性，特此记下。

window.getComputedStyle() 方法

以下是在MDN上查找的方法解释
Window.getComputedStyle()方法返回一个对象，该对象在应用活动样式表并解析这些值可能包含的任何基本计算后报告元素的所有CSS属性的值。 私有的CSS属性值可以通过对象提供的API或通过简单地使用CSS属性名称进行索引来访问。
    let load = document.querySelector('.load');
    let loadb = window.getComputedStyle(load, 'before').width;
