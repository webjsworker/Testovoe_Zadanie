Первый результа по тестовому заданию. На данный момент реализован не весь функционал, для дальнейшего развития проекта 
будет полезно понять по верному ли пути идет разработка. Разработку программы для ПЛК веду первый раз. Выбрал один из пяти промышленных 
стандартов разработки - FBD

Реализованный функционал. 
- на панеле оператора кнопка вкл/выкл. 
- клавиатура задания частоты вращения. (%)
- дисплей мониторинга частоты вражения. (Гц)

Контроллер (описание выбранных блоков)
 Блок OR Включение с кнопки или с панели оператора. 
Блок Sel бинарного выбора. Если G true, то сигнал для старта команда 0001H прямое вражение иначе 0006H
Блок MODW(3) запись значение переменной v1 в частотник 
Блок SC установка значение частоты. 0-100%
Блок MODW(4) запись значения частоты в частотник
Блок MODR чтение значения частоты из частотника
 
IP адреса выбраны стандартые  для ПЛК 192,168,0,2  для панели 192,168,0,200 

Частотник с платой расширения modbus. 

Вопросы возникшие в ходе выполнения работы. 
1 Эмулировать работу панели оператора и контроллера можно из среды разработки только по отдельности ? 
Среда разработки Pro-screen master и pro-logic master. 
Эмулировать работы панели оператора + контроллер + частотник вместе не получится ?  
2 Настройка частотника. Адрес команд  запись A000H чтение B000H. 
Нужно ли конфигурировать частотник на предмет характеристи насоса ? 
Я выбрал управление чатотником по modbus (при добавлении платы расширения в сам частотник) 
или нужно через входы/выходы самого частотника (обратная связь через аналоговые выходы)?

