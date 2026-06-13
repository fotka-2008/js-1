# js-1
💡
1. JavaScript чист?
1
Забони барномасозӣ барои веб
HTML сохтор месозад, CSS зебо мекунад, JS вебсайтро зинда мекунад — тугмаҳо, анимация, маълумот.

2
Ҳама ҷо кор мекунад
Браузер, сервер (Node.js), телефон (React Native), дeskтоп (Electron) — ҳама ҷо JS истифода мешавад.

⚡ JS-ро Brendan Eich дар 10 рӯз навишт — соли 1995!
📦
2. Variables — Тағирёбандаҳо
var
var — кӯҳна, истифода набар
Аввалин роҳ, аммо мушкилот дорад. Дар лоиҳаҳои қадима мебинӣ.

let
let — тағйир меёбад
Агар қиматаш баъдан тағйир меёбад — let истифода бар.

const
const — доимӣ, тағйир намеёбад
Ҳамеша const истифода бар, агар тағйир лозим набошад.

var ism = "Fotima"; // кӯҳна let sin = 20; // тағйир меёбад const PI = 3.14; // доимӣ sin = 21; // ✅ кор мекунад PI = 3; // ❌ хато!
🗂️
3. Data Types — Намудҳои маълумот
Number
Рақамҳо

let x = 42;
let y = 3.14;
String
Матн

let s = "Салом";
let t = 'JS';
Boolean
Рост / дурӯғ

let a = true;
let b = false;
Array
Рӯйхат

let arr = [1, 2, 3];
Object
Объект

{ism: "Ali",
sin: 25}
Null / Undefined
Холӣ / муайян нашуда

let x = null;
let y;
typeof оператор намудро нишон медиҳад: typeof "salom" → "string"
➕
4. Operators — Амалиётҳо
// Арифметикӣ 5 + 3 // 8 10 - 4 // 6 4 * 3 // 12 10 / 2 // 5 10 % 3 // 1 (боқимонда) // Муқоиса 5 == "5" // true (нопок) 5 === "5" // false (тоза ✅) 5 !== 3 // true 5 > 3 // true // Мантиқӣ true && false // false (ва) true || false // true (ё) !true // false (не)
🔀
5. Шартҳо — if / else / switch
let bal = 85; if (bal >= 90) { console.log("Аъло!"); } else if (bal >= 70) { console.log("Хуб!"); } else { console.log("Кӯшиш кун!"); } // Ternary — кӯтоҳ let natija = bal >= 70 ? "Гузашт" : "Нагузашт";
// switch let kun = "Душанбе"; switch (kun) { case "Душанбе": console.log("Аввали ҳафта"); break; case "Ҷумъа": console.log("Охири ҳафта"); break; default: console.log("Рӯзи дигар"); }
🔁
6. Давраҳо — Loops
// for loop for (let i = 0; i < 5; i++) { console.log(i); // 0, 1, 2, 3, 4 } // while loop let i = 0; while (i < 3) { console.log(i); i++; } // for...of — массив учун const мевахо = ["себ", "нок", "анор"]; for (let мева of мевахо) { console.log(мева); } // for...in — объект учун const obj = {a: 1, b: 2}; for (let kalit in obj) { console.log(kalit, obj[kalit]); }
⚙️
7. Функсияҳо — Functions
1
Функсияи оддӣ
function сором(ism) { return "Салом, " + ism + "!"; } console.log(сором("Fotima")); // Салом, Fotima!
2
Arrow Function — муосир ва кӯтоҳ
const сором = (ism) => "Салом, " + ism + "!"; // Чанд сатр const ҷамъ = (a, b) => { return a + b; };
3
Default параметрҳо
function хуш омадед(ism = "Меҳмон") { return "Хуш омадед, " + ism; } хуш омадед(); // Хуш омадед, Меҳмон хуш омадед("Ahmad"); // Хуш омадед, Ahmad
📋
8. Arrays — Массивҳо
const мевахо = ["себ", "нок", "анор"]; мевахо[0] // "себ" мевахо.length // 3 мевахо.push("лиму") // охирга қӯшади мевахо.pop() // охирини олади мевахо.shift() // аввалинро олади мевахо.unshift("узум") // аввалга қӯшади // Муҳимтарин методҳо [1,2,3].map(x => x * 2) // [2,4,6] [1,2,3,4].filter(x => x > 2) // [3,4] [1,2,3].reduce((s,x) => s+x, 0) // 6 [1,2,3].find(x => x > 1) // 2 [1,2,3].includes(2) // true
🗃️
9. Objects — Объектҳо
const talaba = { ism: "Ahmad", sin: 22, дарс: ["JS", "HTML", "CSS"], сором() { return "Ман " + this.ism; } }; talaba.ism // "Ahmad" talaba["sin"] // 22 talaba.сором() // "Ман Ahmad" talaba.шаҳр = "Душанбе"; // нав қӯшидан delete talaba.sin; // ҳазф кардан // Destructuring const { ism, sin } = talaba; // Spread operator const нав = { ...talaba, синф: "A1" };
🖥️
10. DOM — HTML-ро идора кун
// Элементро гир document.getElementById("id_ман") document.querySelector(".класс") document.querySelectorAll("p") // Матнро тағйир деҳ const el = document.getElementById("sarlavha"); el.textContent = "Салом Ҷаҳон!"; el.innerHTML = "<b>Ғафс матн</b>"; // Стилро тағйир деҳ el.style.color = "red"; el.style.fontSize = "24px"; // Класс el.classList.add("фаъол"); el.classList.remove("фаъол"); el.classList.toggle("фаъол"); // Элементи нав сохт const div = document.createElement("div"); div.textContent = "Нав!"; document.body.appendChild(div);
🖱️
11. Events — Ҳодисаҳо
const btn = document.getElementById("tugma"); // Клик btn.addEventListener("click", () => { console.log("Тугма пахш шуд!"); }); // Input тағйир const input = document.querySelector("input"); input.addEventListener("input", (e) => { console.log(e.target.value); }); // Саҳифа бор шуд document.addEventListener("DOMContentLoaded", () => { console.log("Саҳифа тайёр!"); });
📝 Маъмултарин ҳодисаҳо: click, input, change, submit, keydown, mouseover, load
⏳
12. Async / Await — Ваъда
1
Promise
const ваъда = new Promise((resolve, reject) => { let муваффақ = true; if (муваффақ) resolve("Кор кард!"); else reject("Хато!"); }); ваъда .then(natija => console.log(natija)) .catch(хато => console.log(хато));
2
Async / Await — осонтар
async function маълумотГир() { try { const javob = await fetch("https://api.example.com"); const data = await javob.json(); console.log(data); } catch (хато) { console.log("Хато:", хато); } }
✨
13. ES6+ — Хусусиятҳои муосир
// Template literals const ism = "Ahmad"; console.log(`Салом, ${ism}! Синат ${22} аст.`); // Destructuring const [a, b, c] = [1, 2, 3]; const { ism: nom, sin } = { ism: "Ali", sin: 25 }; // Spread & Rest const arr1 = [1, 2]; const arr2 = [...arr1, 3, 4]; // [1,2,3,4] function ҷамъ(...рақамҳо) { return рақамҳо.reduce((s, x) => s + x, 0); } // Optional chaining const шаҳр = корбар?.манзил?.шаҳр; // Nullish coalescing const ном = корбар ?? "Меҳмон";
🗺️
14. Роҳи омӯзиш — қадам ба қадам
1
Variables, Types, Operators
Асос — ҳамаи чиз аз инҷо оғоз мешавад. Ин қадамро нағз омӯз.

2
if/else, loops, functions
Мантиқи барнома — шартҳо, давраҳо, функсияҳо.

3
Arrays & Objects
Маълумотро нигоҳ дор ва идора кун.

4
DOM manipulation & Events
HTML-ро бо JS зинда кун — тугмаҳо, форма, анимация.

5
Async, Fetch, API
Серверҳо бо JS — маълумот аз интернет гир.

6
React / Vue / Node.js
Сатҳи баланд — фреймворкҳо ва backend.

Variables Functions Arrays Objects DOM Events Async/Await ES6+ Node.js React
Тартиб додааст JavaScript Guide TJ — аз аввал то охир 🚀