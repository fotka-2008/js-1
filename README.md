# js-1
JavaScript — Полное руководство


Всё о JavaScript от начала до конца — шаг за шагом




📌 Содержание


Что такое JavaScript
Переменные — Variables
Типы данных — Data Types
Операторы — Operators
Условия — if / else / switch
Циклы — Loops
Функции — Functions
Массивы — Arrays
Объекты — Objects
DOM — управление HTML
События — Events
Async / Await
ES6+ — современные возможности
Путь обучения — Roadmap



1. Что такое JavaScript

JavaScript — язык программирования для веба.


HTML создаёт структуру
CSS делает красиво
JS оживляет сайт — кнопки, анимации, данные


JavaScript работает везде:

СредаИнструментБраузерChrome, Firefox, SafariСерверNode.jsТелефонReact NativeДесктопElectron


⚡ JavaScript создал Brendan Eich за 10 дней в 1995 году.




2. Переменные — Variables

Три способа объявить переменную:

jsvar ism = "Fotima";   // устарело
let yosh = 20;        // меняется
const PI = 3.14;      // постоянная

Ключевое словоМеняется?Область видимостиИспользовать?var✅функция❌ устарелоlet✅блок✅ даconst❌блок✅ по умолчанию


💡 Всегда используй const. Переходи на let только если значение нужно менять.




3. Типы данных — Data Types

js// Number — числа
let x = 42;
let y = 3.14;

// String — текст
let ism = "Fotima";
let shahar = 'Dushanbe';
let jumlа = `Привет, ${ism}!`;  // шаблон

// Boolean — да / нет
let faol = true;
let band = false;

// Array — список
let mevalar = ["себ", "нок", "анор"];

// Object — объект
let talaba = { ism: "Ali", yosh: 22 };

// Null — пусто (намеренно)
let natija = null;

// Undefined — не задано
let noma;
console.log(noma); // undefined

Проверить тип:

jstypeof "salom"   // "string"
typeof 42        // "number"
typeof true      // "boolean"
typeof []        // "object"
typeof null      // "object" (особенность JS!)


4. Операторы — Operators

Арифметические

js5 + 3    // 8
10 - 4   // 6
4 * 3    // 12
10 / 2   // 5
10 % 3   // 1 (остаток)
2 ** 3   // 8 (степень)

Сравнение

js5 == "5"   // true  — нестрогое (не рекомендуется)
5 === "5"  // false — строгое ✅
5 !== 3    // true
5 > 3      // true
5 >= 5     // true

Логические

jstrue && false  // false — И
true || false  // true  — ИЛИ
!true          // false — НЕ


5. Условия — if / else / switch

if / else if / else

jslet ball = 85;

if (ball >= 90) {
  console.log("Отлично!");
} else if (ball >= 70) {
  console.log("Хорошо!");
} else {
  console.log("Попробуй ещё!");
}

Тернарный оператор

jslet natija = ball >= 70 ? "Сдал" : "Не сдал";

switch

jslet kun = "Понедельник";

switch (kun) {
  case "Понедельник":
    console.log("Начало недели");
    break;
  case "Пятница":
    console.log("Конец недели");
    break;
  default:
    console.log("Другой день");
}


6. Циклы — Loops

for

jsfor (let i = 0; i < 5; i++) {
  console.log(i); // 0, 1, 2, 3, 4
}

while

jslet i = 0;
while (i < 3) {
  console.log(i);
  i++;
}

for...of — для массивов

jsconst mevalar = ["себ", "нок", "анор"];

for (let meva of mevalar) {
  console.log(meva);
}

for...in — для объектов

jsconst obj = { a: 1, b: 2, c: 3 };

for (let kalit in obj) {
  console.log(kalit, obj[kalit]);
}


7. Функции — Functions

Обычная функция

jsfunction salom(ism) {
  return "Привет, " + ism + "!";
}

console.log(salom("Fotima")); // Привет, Fotima!

Стрелочная функция (ES6)

jsconst salom = (ism) => "Привет, " + ism + "!";

// Несколько строк
const yigindi = (a, b) => {
  return a + b;
};

Параметры по умолчанию

jsfunction xushomadid(ism = "Гость") {
  return "Добро пожаловать, " + ism;
}

xushomadid();          // Добро пожаловать, Гость
xushomadid("Ahmad");   // Добро пожаловать, Ahmad


8. Массивы — Arrays

jsconst mevalar = ["себ", "нок", "анор"];

mevalar[0]             // "себ"
mevalar.length         // 3
mevalar.push("лимон")  // добавить в конец
mevalar.pop()          // удалить с конца
mevalar.shift()        // удалить с начала
mevalar.unshift("узум") // добавить в начало

Основные методы

js// map() — преобразовать каждый элемент
[1, 2, 3].map(x => x * 2)         // [2, 4, 6]

// filter() — отфильтровать
[1, 2, 3, 4].filter(x => x > 2)   // [3, 4]

// reduce() — свернуть в одно значение
[1, 2, 3].reduce((s, x) => s + x, 0) // 6

// find() — найти первый элемент
[1, 2, 3].find(x => x > 1)        // 2

// includes() — проверить наличие
[1, 2, 3].includes(2)             // true

// forEach() — перебрать
[1, 2, 3].forEach(x => console.log(x))

// sort() — сортировка
[3, 1, 2].sort((a, b) => a - b)   // [1, 2, 3]


9. Объекты — Objects

jsconst talaba = {
  ism: "Ahmad",
  yosh: 22,
  darslar: ["JS", "HTML", "CSS"],
  salom() {
    return "Я " + this.ism;
  }
};

talaba.ism            // "Ahmad"
talaba["yosh"]        // 22
talaba.salom()        // "Я Ahmad"
talaba.shahar = "Душанбе"; // добавить поле
delete talaba.yosh;   // удалить поле

Деструктуризация

jsconst { ism, yosh } = talaba;

Spread оператор

jsconst yangi = { ...talaba, sinf: "A1" };


10. DOM — управление HTML

js// Получить элемент
const el = document.getElementById("sarlavha");
const el = document.querySelector(".klass");
const els = document.querySelectorAll("p");

// Изменить текст
el.textContent = "Привет, мир!";
el.innerHTML = "<b>Жирный текст</b>";

// Изменить стиль
el.style.color = "red";
el.style.fontSize = "24px";

// Работа с классами
el.classList.add("faol");
el.classList.remove("faol");
el.classList.toggle("faol");

// Создать новый элемент
const div = document.createElement("div");
div.textContent = "Новый!";
document.body.appendChild(div);


11. События — Events

jsconst btn = document.getElementById("tugma");

// Клик
btn.addEventListener("click", () => {
  console.log("Кнопка нажата!");
});

// Изменение input
const input = document.querySelector("input");
input.addEventListener("input", (e) => {
  console.log(e.target.value);
});

// Загрузка страницы
document.addEventListener("DOMContentLoaded", () => {
  console.log("Страница готова!");
});

Часто используемые события:

СобытиеКогдаclickклик мышьюinputизменение поля вводаchangeизменение значенияsubmitотправка формыkeydownнажатие клавишиmouseoverнаведение мышиloadзагрузка страницы


12. Async / Await

Promise

jsconst vaada = new Promise((resolve, reject) => {
  let muvaffaq = true;
  if (muvaffaq) resolve("Успешно!");
  else reject("Ошибка!");
});

vaada
  .then(natija => console.log(natija))
  .catch(xato => console.log(xato));

Async / Await — проще и чище

jsasync function malumotOl() {
  try {
    const javob = await fetch("https://api.example.com/data");
    const data = await javob.json();
    console.log(data);
  } catch (xato) {
    console.log("Ошибка:", xato);
  }
}

malumotOl();


13. ES6+ — современные возможности

Шаблонные строки

jsconst ism = "Ahmad";
console.log(`Привет, ${ism}! Тебе ${22} лет.`);

Деструктуризация

js// Массив
const [a, b, c] = [1, 2, 3];

// Объект
const { ism, yosh } = { ism: "Ali", yosh: 25 };

Spread и Rest

js// Spread — разворачивает
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4]; // [1, 2, 3, 4]

// Rest — собирает
function yigindi(...raqamlar) {
  return raqamlar.reduce((s, x) => s + x, 0);
}

Optional Chaining

jsconst shahar = foydalanuvchi?.manzil?.shahar;
// не выдаёт ошибку если manzil не существует

Nullish Coalescing

jsconst nom = foydalanuvchi ?? "Гость";
// "Гость" только если foydalanuvchi — null или undefined


14. Путь обучения — Roadmap

Шаг 1 → Variables, Types, Operators
         (Основа — начни отсюда)

Шаг 2 → if/else, Loops, Functions
         (Логика программы)

Шаг 3 → Arrays & Objects
         (Хранение данных)

Шаг 4 → DOM & Events
         (Оживи HTML с JS)

Шаг 5 → Async, Fetch, API
         (Данные из интернета)

Шаг 6 → React / Vue / Node.js
         (Продвинутый уровень)


Теги

Variables Functions Arrays Objects DOM Events Async/Await ES6+ Node.js React


JavaScript — самый популярный язык программирования в мире. Учись каждый день! 🚀