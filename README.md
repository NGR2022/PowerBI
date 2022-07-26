# PowerBI
- Для данного примера были использованы случайные данные: таблица "Сделки" (в приложенных файлах для загрузки - файл "таблица с данными сделок "), Стоимость продвижения" (приложен файл "таблица с допданными"). 
 	В таблицу "Сделки" в рамках PowerBI добавлены вычисляемые столбцы "Сумма сделок, USD" и "Дни недели" 

- Использовался сайт ЦБ РФ для получения данных по курсам валют (в данной работе основной целью использования данного источника было показать владение этой опцией Power BI). Ссылки приведены в самом конце. 
- Создана таблица "Общая таблица курсов". Она содержит в себе курсы трех валют: USD, EURO, CNY. Создана путем слияния таблиц. 
	Даты в этой таблице идут без пропусков, т.е. все, включая выходные и праздничные дни. Т.к. курсы на сайте ЦБ РФ даны только для банковских дней, то в "Общей таблице курсов" курсы на небанковские дни заполнены по курсам последнего банковского дня накануне нерабочих. Т.е. например, курс на Сб и Вс такой же, как курс на Пт.
	Также добавлены столбцы  по курсам на 1 единицу. Это связано с тем, что курс CNY дается на сайте то на 1, то на 10 единиц.

- Создана таблица-календарь через опцию "Создать таблицу". В ней использовала функции даты и времени DAX.
в работе с отчетом (графиками) создавала Меры для визуализаций. 
привожу ниже функции DAX, которые использовались в этом файле:
CALCULATE, USERELATIONSHIP, RELATED, FILTER, AND, FORMAT, SWITCH

COUNT, DISTINCTCOUNT, COUNTA

SUM, SUMX, DIVIDE

MAXX, MEDIANX, MEDIAN

ALL, ALLSELECTED

DATEDIFF, TODAY, DAY, MONTH, QUATER, WEEKDAY, WEEKNUM, CALENDAR

Таблица "Сделки" - таблица фактов
остальные - таблицы измерений
схема связей таблиц имеет схему снежинки

 Курс Китайского Юаня

https://cbr.ru/currency_base/dynamics/?UniDbQuery.Posted=True&UniDbQuery.so=1&UniDbQuery.mode=1&UniDbQuery.date_req1=&UniDbQuery.date_req2=&UniDbQuery.VAL_NM_RQ=R01375&UniDbQuery.From=01.02.2022&UniDbQuery.To=12.07.2022



Курс Доллара США

https://cbr.ru/currency_base/dynamics/?UniDbQuery.Posted=True&UniDbQuery.so=1&UniDbQuery.mode=1&UniDbQuery.date_req1=&UniDbQuery.date_req2=&UniDbQuery.VAL_NM_RQ=R01235&UniDbQuery.From=01.02.2022&UniDbQuery.To=12.07.2022



Курс Евро

https://cbr.ru/currency_base/dynamics/?UniDbQuery.Posted=True&UniDbQuery.so=1&UniDbQuery.mode=1&UniDbQuery.date_req1=&UniDbQuery.date_req2=&UniDbQuery.VAL_NM_RQ=R01239&UniDbQuery.From=01.02.2022&UniDbQuery.To=12.07.2022
