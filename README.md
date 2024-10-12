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
    <img src="https://github.com/user-attachments/assets/6510dc57-b82c-484f-bd6d-ecf6b219cce6" width="202"> 
    <img src="https://github.com/user-attachments/assets/a6f3a4bb-bcdf-4bb1-bc1a-8744ff309d0e" width="200">
    <img src="[https://github.com/user-attachments/assets/79405b8c-7b46-46c1-a729-f8e177c0c569](https://private-user-images.githubusercontent.com/163531602/375938560-45691fb1-1eda-4e14-92e1-3874bbf83165.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MTk5MzQsIm5iZiI6MTcyODcxOTYzNCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYwLTQ1NjkxZmIxLTFlZGEtNGUxNC05MmUxLTM4NzRiYmY4MzE2NS5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzUzNTRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1mNGVmODg0Y2E2YjU3YWYyZGU5NWZlZTU2MGVkNjg3ODU0YjYwOTIwYzBhN2FhNjg2MDczYzUxZTZiN2I1MWU0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.sksaFaapP45aJ8dThpZMdwsrPNEDkbeNL4fnqO5jIbQ)" width="200"> 
    <img src="https://github.com/user-attachments/assets/030819f6-b9e5-4537-b3ae-2383075f3236" width="200">
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
    <img src="https://github.com/user-attachments/assets/6510dc57-b82c-484f-bd6d-ecf6b219cce6" width="200"> 
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
    <img src="https://github.com/user-attachments/assets/a6f3a4bb-bcdf-4bb1-bc1a-8744ff309d0e" width="200">
</p> 


---

### <a id="activity3"> Экран 3 (ThirdActivity)</a>
**_Особенность экрана:_** сверстан с использованием `RelativeLayout`, т.е. местоположение объектов задается относительно других.

**Состоит из 6 кнопок:**
- 2 расположены в верхней части экрана и занимают по половине экрана
- 3 расположены по центру
- 1 расположена в нижней части экрана

<p align="center">
    <img src="https://github.com/user-attachments/assets/79405b8c-7b46-46c1-a729-f8e177c0c569" width="200"> 
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
    <img src="https://github.com/user-attachments/assets/030819f6-b9e5-4537-b3ae-2383075f3236" width="200">
    <img src="https://github.com/user-attachments/assets/be6b908c-725e-41c0-b86a-35ab256a5481" width="200"> 
</p> 



