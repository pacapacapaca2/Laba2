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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938566-14bcbba1-484f-4d14-b8fd-b26c02bc1276.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY2LTE0YmNiYmExLTQ4NGYtNGQxNC1iOGZkLWIyNmMwMmJjMTI3Ni5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03MDk5NzljZjZiZjE5ODRlZDI0NTU4NDUwZmVkZjJkNTdlYmVhNTcwNmZiZDkyM2JmZGJiZDY1YTA4YmI0ZThmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.GeHGuW_pvANhxs3q0pnSKS7gag7MrFgArTCVBvfwz_E" width="202"> 
    <img src="https://private-user-images.githubusercontent.com/163531602/375938564-c5b4e26d-7764-447d-ac16-4a2d28a20353.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY0LWM1YjRlMjZkLTc3NjQtNDQ3ZC1hYzE2LTRhMmQyOGEyMDM1My5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05MmUzMzRjOGZkMTJkYjhiZjkwZDc5YmU0ODIxNTJjNzUwZjk5OWJhMjZhMGFmMDczZTBjNjcwYmIwNzY1ZmM5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.9C9O561_uLpS4mJg5QddWrqB0zuWpF7hDjamJDKF75s" width="200">
    <img src="https://private-user-images.githubusercontent.com/163531602/375938560-45691fb1-1eda-4e14-92e1-3874bbf83165.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYwLTQ1NjkxZmIxLTFlZGEtNGUxNC05MmUxLTM4NzRiYmY4MzE2NS5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xNzNiNTMxZDViMmQ1MDE2YjQ0ZWJjMmZjZDZhNjU5MThlOTFhZjdmNGI5NzBhNzNmZmY4ODZjMGQ1ZDdkYzMxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.zWeALn4hnkynXOxwz4uY8dS1sEHly-5ZjaJsGK0fXT4" width="200"> 
    <img src="https://private-user-images.githubusercontent.com/163531602/375938562-5533f75e-b65e-4893-acfc-f86068a58828.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYyLTU1MzNmNzVlLWI2NWUtNDg5My1hY2ZjLWY4NjA2OGE1ODgyOC5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1jODlkMTUzMzU3ZTdkMGNiYWI2ZTI4MWM2NjU3ZWM0NWQ1NzczMDdiMTU1YmQyMWZiNDI0NjVhZTFlMzNlZTMzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.uJRR3G_I-Ozcnaaw8brIj3pCMwW5A6ntBAmDyqJ9q1c" width="200">
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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938566-14bcbba1-484f-4d14-b8fd-b26c02bc1276.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY2LTE0YmNiYmExLTQ4NGYtNGQxNC1iOGZkLWIyNmMwMmJjMTI3Ni5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03MDk5NzljZjZiZjE5ODRlZDI0NTU4NDUwZmVkZjJkNTdlYmVhNTcwNmZiZDkyM2JmZGJiZDY1YTA4YmI0ZThmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.GeHGuW_pvANhxs3q0pnSKS7gag7MrFgArTCVBvfwz_E" width="200"> 
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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938564-c5b4e26d-7764-447d-ac16-4a2d28a20353.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY0LWM1YjRlMjZkLTc3NjQtNDQ3ZC1hYzE2LTRhMmQyOGEyMDM1My5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05MmUzMzRjOGZkMTJkYjhiZjkwZDc5YmU0ODIxNTJjNzUwZjk5OWJhMjZhMGFmMDczZTBjNjcwYmIwNzY1ZmM5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.9C9O561_uLpS4mJg5QddWrqB0zuWpF7hDjamJDKF75s" width="200">
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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938562-5533f75e-b65e-4893-acfc-f86068a58828.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYyLTU1MzNmNzVlLWI2NWUtNDg5My1hY2ZjLWY4NjA2OGE1ODgyOC5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1jODlkMTUzMzU3ZTdkMGNiYWI2ZTI4MWM2NjU3ZWM0NWQ1NzczMDdiMTU1YmQyMWZiNDI0NjVhZTFlMzNlZTMzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.uJRR3G_I-Ozcnaaw8brIj3pCMwW5A6ntBAmDyqJ9q1c" width="200">
    <img src="https://private-user-images.githubusercontent.com/163531602/375938561-12eb1d00-0e72-42e9-80ff-69b690f94533.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mjg3MjAwMjgsIm5iZiI6MTcyODcxOTcyOCwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYxLTEyZWIxZDAwLTBlNzItNDJlOS04MGZmLTY5YjY5MGY5NDUzMy5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxMlQwNzU1MjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT00NmJmMDZiMWVkMDJjZWY0MTg2NzlkYzViMDdiZDZjZDAxMjEwZDBiNDZmN2ExZWY0OTUxMWZhZmVlYjNhOWM4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.9Ru_xsnnJ9CpZdIzjNBhJjJpgzM03DTjjhVlrFs_FKA" width="200"> 
</p> 



