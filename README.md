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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938566-14bcbba1-484f-4d14-b8fd-b26c02bc1276.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY2LTE0YmNiYmExLTQ4NGYtNGQxNC1iOGZkLWIyNmMwMmJjMTI3Ni5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNmYxYzlhYjI1YmI0YTI0NzgzMzFhODVmNDlkOTYzMzFkZTExMjUxNjNkYjMzYjk4NzhjZjVhYmE5NzczMTNhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.CCd06wqbojxheDF1z098Bp-87o72x5SEUSzRA6L_TRU" width="202"> 
    <img src="https://private-user-images.githubusercontent.com/163531602/375938564-c5b4e26d-7764-447d-ac16-4a2d28a20353.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY0LWM1YjRlMjZkLTc3NjQtNDQ3ZC1hYzE2LTRhMmQyOGEyMDM1My5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05NDNiYjY5Y2ZlNDQwZDM0NWQ5ZGU1NGI1MmZkYmFiMjRkYmU5MzhhODdlYWViYTZiMGRiZWM5ZTlmY2ZhMjcyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.Nw_Hq4_ifvlc3P5Hma6tMJGfauSuwZGSlaa2yKE2xZ0" width="200">
    <img src="https://private-user-images.githubusercontent.com/163531602/375938560-45691fb1-1eda-4e14-92e1-3874bbf83165.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYwLTQ1NjkxZmIxLTFlZGEtNGUxNC05MmUxLTM4NzRiYmY4MzE2NS5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNTVmMGYyYzVlMjliMzc5YWJmNTAwNjYyMGVmMWVlNTg4MmY4ZDI2N2JiMDA0OWY4ZWE1MzgyZGNiMGY5MWIxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.ECNkSAsq9o0POtF9JTVqyjeCHbVFUASmZE9rWwgwoVg" width="200"> 
    <img src="https://private-user-images.githubusercontent.com/163531602/375938562-5533f75e-b65e-4893-acfc-f86068a58828.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYyLTU1MzNmNzVlLWI2NWUtNDg5My1hY2ZjLWY4NjA2OGE1ODgyOC5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04YjQ5NTBkOWU4M2M0Mzc2NzU1YzNmMjVlODljMDQ2YzZhNWQ5Y2U4MjliMTExOWU0MGIyNjUwYzJkNDg3ZWE5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.shNBmW7IIEYFGX5c8A-3nQ3BDAgxdvhtdHy0s03lse8" width="200">
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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938566-14bcbba1-484f-4d14-b8fd-b26c02bc1276.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY2LTE0YmNiYmExLTQ4NGYtNGQxNC1iOGZkLWIyNmMwMmJjMTI3Ni5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNmYxYzlhYjI1YmI0YTI0NzgzMzFhODVmNDlkOTYzMzFkZTExMjUxNjNkYjMzYjk4NzhjZjVhYmE5NzczMTNhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.CCd06wqbojxheDF1z098Bp-87o72x5SEUSzRA6L_TRU" width="200"> 
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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938564-c5b4e26d-7764-447d-ac16-4a2d28a20353.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTY0LWM1YjRlMjZkLTc3NjQtNDQ3ZC1hYzE2LTRhMmQyOGEyMDM1My5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05NDNiYjY5Y2ZlNDQwZDM0NWQ5ZGU1NGI1MmZkYmFiMjRkYmU5MzhhODdlYWViYTZiMGRiZWM5ZTlmY2ZhMjcyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.Nw_Hq4_ifvlc3P5Hma6tMJGfauSuwZGSlaa2yKE2xZ0" width="200">
</p> 


---

### <a id="activity3"> Экран 3 (ThirdActivity)</a>
**_Особенность экрана:_** сверстан с использованием `RelativeLayout`, т.е. местоположение объектов задается относительно других.

**Состоит из 6 кнопок:**
- 2 расположены в верхней части экрана и занимают по половине экрана
- 3 расположены по центру
- 1 расположена в нижней части экрана

<p align="center">
    <img src="https://private-user-images.githubusercontent.com/163531602/375938560-45691fb1-1eda-4e14-92e1-3874bbf83165.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYwLTQ1NjkxZmIxLTFlZGEtNGUxNC05MmUxLTM4NzRiYmY4MzE2NS5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNTVmMGYyYzVlMjliMzc5YWJmNTAwNjYyMGVmMWVlNTg4MmY4ZDI2N2JiMDA0OWY4ZWE1MzgyZGNiMGY5MWIxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.ECNkSAsq9o0POtF9JTVqyjeCHbVFUASmZE9rWwgwoVg" width="200"> 
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
    <img src="https://private-user-images.githubusercontent.com/163531602/375938562-5533f75e-b65e-4893-acfc-f86068a58828.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYyLTU1MzNmNzVlLWI2NWUtNDg5My1hY2ZjLWY4NjA2OGE1ODgyOC5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04YjQ5NTBkOWU4M2M0Mzc2NzU1YzNmMjVlODljMDQ2YzZhNWQ5Y2U4MjliMTExOWU0MGIyNjUwYzJkNDg3ZWE5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.shNBmW7IIEYFGX5c8A-3nQ3BDAgxdvhtdHy0s03lse8" width="200">
    <img src="https://private-user-images.githubusercontent.com/163531602/375938561-12eb1d00-0e72-42e9-80ff-69b690f94533.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjkxODU2ODksIm5iZiI6MTcyOTE4NTM4OSwicGF0aCI6Ii8xNjM1MzE2MDIvMzc1OTM4NTYxLTEyZWIxZDAwLTBlNzItNDJlOS04MGZmLTY5YjY5MGY5NDUzMy5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQxMDE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MTAxN1QxNzE2MjlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01ZjFlYjhkYjkyOWFhNTA0Nzk5Yjk1MTQxMGE0MmFmYTFjMGFmZmM4ZGM3NjUyYzVkYzFhNGFjNDkwZmZkY2U5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.QSYtWEotrDgdO3Fjz5t0aICUiGy5OkiDlWqtIQ8lBa8" width="200"> 
</p> 



