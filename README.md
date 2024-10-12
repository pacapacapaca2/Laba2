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
    <img src="https://github.com/user-attachments/assets/79405b8c-7b46-46c1-a729-f8e177c0c569" width="200"> 
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

_**Общее по кнопкам:**_
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

Для задания размеров и положения использовались следующие **свойства `LinearLayout`**:
- `android:layout_weight` // отвечает за соотношение размеров между элементами
- `android:layout_gravity` // указывает расположение внутри `LinearLayout`

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

Для задания размеров и положения использовались следующие **свойства `RelativeLayout`**:
- _относительно родительского `RelativeLayout`_:
  - `android:layout_alignParentStart="true"` // левый верхний угол
  - `android:layout_alignParentRight="true"` // правый верхний угол
  - `android:layout_centerInParent="true"` // центр
  - `android:layout_alignParentBottom="true"` // нижняя часть
- _относительно других объектов:_
  - `android:layout_toLeftOf = "@+id/.."` // "Left 50%" и "Center_left"
  - `android:layout_toRightOf="@+id/.."` // "Right 50%" и "Center_right"


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

Для выполнения выше указанных условий был создан файл `my_button_bg` внутри папки `drawable`:
- т.к. при нажатии цвет должен изменяться, используется класс `selector`, включающий в себя 2 объекта `item` (для состояния "нажато" и "не нажато").
- каждый объект имеет одинаковую структуру:
  - ``` java
      <item android:state_focused="false"
        android:state_pressed="true" // если объект не нажат, то будет false
        android:state_enabled="true">
        <shape xmlns:android="http://schemas.android.com/apk/res/android"
        android:shape="rectangle" > // создается фигура прямоугольник
            <solid android:color="@android:color/holo_green_light" /> // указывается цвет фигуры
            <corners android:radius="24dp"/> // определяется радиус скругления
            <stroke android:width="10px" android:color="#505050" /> // задается толщина и цвет обводки
        </shape>
      </item>
      ```

Чтобы подтянулись все параметры, внутри файла с версткой экрана (`activity_fourth.xml`) указано следующее:
- `android:background="@drawable/my_button_bg"` // фон кнопки
- `android:drawableLeft="@drawable/ic_launcher_foreground"` // добавление иконки в левой части кнопки


