# Лабораторная работа №2. Основы верстки
- _Выполнил:_ Стан
- _Язык программирования:_ Java

## Что делает приложение?
Приложение состоит из 4 экранов:
1. [Меню](#activity1).
2. [Экран 2](#activity2), который сверстан с использованием `LinearLayout`.
3. [Экран 3](#activity3), который сверстан с использованием `RelativeLayout`.
4. [Экран 4](#activity4).

<p align="center">
    <img src="https://github.com/user-attachments/assets/14bcbba1-484f-4d14-b8fd-b26c02bc1276" width="202"> 
    <img src="https://github.com/user-attachments/assets/c5b4e26d-7764-447d-ac16-4a2d28a20353" width="200">
    <img src="https://github.com/user-attachments/assets/45691fb1-1eda-4e14-92e1-3874bbf83165" width="200"> 
    <img src="https://github.com/user-attachments/assets/5533f75e-b65e-4893-acfc-f86068a58828" width="200">
</p> 
Возврат на предыдущий экран осуществляется при помощи системной кнопки / бэксвайпа

---
### <a id="activity1"> Меню (экран 1) </a>

**_Меню состоит из 4х кнопок:_**
- **"Экран 2"**. - > открытие [`SecondActivity`](#activity2)
- **"Экран 3"**. -> открытие [`ThirdActivity`](#activity3)
- **"Экран 4"**. -> открытие [`FourthActivity`](#activity4)
- **"Выйти"**. -> выход из приложения.

_**Характеристики кнопок:**_
- высота каждой кнопки составляет **20%** от высоты экрана
- расстояние между кнопками - **2%**
- ширина кнопок - **75%**
- расстояние от первой кнопки до верхнего края **==** расстоянию от последней кнопки до нижнего края **== 7%**
- кнопки выровнены по центру.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/14bcbba1-484f-4d14-b8fd-b26c02bc1276" width="200"> 
</p> 

---
### <a id="activity2"> Экран 2 (SecondActivity)</a>
**Особенность экрана:** сверстан с использованием `LinearLayout`.

**Состоит из 7 кнопок:**
- 3 расположены в верхней части экрана и занимают равную ширину
- 2 расположены по центру, занимают равные части, но имеют отступы от краев
- 3 расположены в нижней части экрана:
  - 1 занимает половину всей ширины экрана
  - 2 делят оставшуюся часть поровну между собой
  <p align="center">
    <img src="https://github.com/user-attachments/assets/c5b4e26d-7764-447d-ac16-4a2d28a20353" width="200">
</p> 


---

### <a id="activity3"> Экран 3 (ThirdActivity)</a>
**_Особенность экрана:_** сверстан с использованием `RelativeLayout`, т.е. местоположение объектов задается относительно других.

**Состоит из 6 кнопок:**
- 2 расположены в верхней части экрана и занимают по половине экрана
- 3 расположены по центру
- 1 расположена в нижней части экрана

<p align="center">
    <img src="https://github.com/user-attachments/assets/45691fb1-1eda-4e14-92e1-3874bbf83165" width="200"> 
</p> 

 ---
### <a id="activity4"> Экран 4 (FourthActivity)</a>

На экране расположена всего 1 кнопка. Ее особенности:
- выровнена по центру экрана
- имеет темно-зеленый цвет
- слева от текста изображена иконка приложения
- цвет обводки кнопки `#505050`
- толщина обводки `10px` (т.к. я родился в октябре)
- радиус скругления кнопки `24dp`
- при нажатии на кнопку ее цвет изменяется на светло-зеленый.
<p align="center">
    <img src="https://github.com/user-attachments/assets/5533f75e-b65e-4893-acfc-f86068a58828" width="200">
    <img src="https://github.com/user-attachments/assets/12eb1d00-0e72-42e9-80ff-69b690f94533" width="200"> 
</p> 



