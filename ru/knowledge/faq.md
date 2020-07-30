---
layout: page
title: FAQ
parent: Знания
nav_exclude: true
---

### FAQ

Эта страница содержит список часто-задаваемых вопросов в комьюнити технического бедрока, которые не заслужили отдельных статей. Ваши вопросы/ответы всегда приветствуются, как и любая другая помощь!

`Совет:` Используйте Ctrl+F (поиск по странице), чтобы быстро найти нужное.

---

### Как мне убрать яйцо спавна сущности из меню креатива?

 - Сделайте компонент spawnable на false внутри файла параметров (Behavior)
 - И удалите spawn egg компонент внутри файла ресурсов (Resource)

---

### Какое friction у блоков по умолчанию?
0.5

---

### Могу ли я сделать свои блоки прозрачными?
Нет

---

### Как сделать повторяющуюся анимацию?
Зациклите анимацию (флаг loop) и не давайте ей перейти в другую анимацию

---

### Где я могу найти логи ошибок/вывода (в Windows)?
`C:\Users\YOUR_USERNAME\AppData\Local\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\logs`

---
### Как я могу сделать полностью невидимую тень у сущности, без изменения collision box'а? 
 - а) используйте runtime от armor stand
 - б) измените shadow.material

---
### А как я могу убрать облака?
Изменить текстуру облаов в ресурс-паке на полностью прозрачную

---
### Можно ли добавить отдачу атаке сущности без использования minecraft:behavior.knockback_roar?
Нет
 
---
### Можно ли сделать свой блок, смотрящий в определёную сторону?
Нет

---
### Как узнать, находится ли игрок в Аду или Краю?
Никак

---
### Как мне запретить толкать сущность?
```json
"minecraft:push_through": {
  "value": 0
}
```

---
### Как запретить сущности сдвигаться водой?
Никак

---
### Переменные сохраняются?
Нет, они сбрасываются когда сущность выгружается из памяти (как при выходе из мира, или выгрузке чанка)

---
### Как заставить моего моба светиться?
Используйте `entity_emissive` или `entity_emissive_alpha` материал, он использует альфа-слой изображений, чтобы заставлять вещи "светиться". Посмотрите на глаза паука например.

---
### Возможно ли выдать себе спавнер с мобом внутри?
Нет

---
### Возможно ли сделать "on_entry":["/execute @e[name=variable.some_name] ..."]?
Нет

---
### Где я могу скачать ресурсы MCBE?
[Ресурсы MCBE находяться здесь](https://discordapp.com/channels/523663022053392405/523663022498250762/715962598843089008).

---
### Возможно ли наносить урон сущности, только когда держишь определёную вещь?
Создайте damage_sensor и выставьте deals_damage на false когда держат не эту вещь.

---
### Где можно найти список переменных в molang?
[Список переменных в molang](https://bedrock.dev/1.14.0.0/1.14.30.51/MoLang).

---
### Можно ли использовать /give чтобы получить шалкер-ящик с вещами?
 - Нет
 - Обход: Скопируйте сундук игроку и /fill уберите его
 - Другой обход: создайте сущность-пустышку с нужной лут-таблицей, и затем убейте её.

---
### Какой максимум секунд в /effect команде?
 - 2147483647