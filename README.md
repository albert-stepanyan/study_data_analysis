# Исследование объявлений о продаже квартир

В вашем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Ваша задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность. 

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма. 

## Описание данных

Предоставлен файл (real_estate.csv) с находящимся в нем архивом объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктах за несколько лет.

## План работы

О качестве данных ничего не известно, кроме того, что одна часть информации была указана пользователями самостоятельно, другая - получена автоматически на основе картографических данных (например, расстояние до центра, аэропорта, ближайшего парка и водоёма).

Мы проверим данные на ошибки и оценим их влияние на исследование; затем, на этапе предобработки поищем возможность исправить самые критичные ошибки. Далее проведем расчеты, на основании которых проанализируем данные и выявим параметры, влияющие на ценообразование квартиры.

Таким образом, исследование пройдёт в четыре этапа:

- Обзор данных
- Предобработка данных
- Расчеты
- Исследовательский анализ данных

## Общий вывод

Мы определили, что датафрейм содержит объявления о продаже недвижимости в Санкт-Петербурге и области за период с 27 ноября 2014 по 3 мая 2019 годов. Резкий рост продаж начался с февраля 2017 года. Мы убрали артефакты, частично заполнили пропуски в данных, изменили формат столбцов.

- При анализе значений по стоимости квартир были удалены 0.15% данных принятые за артефакты. Что значительно меньше допустимых 10%.
- Самое распростроненное количество фотографий это от 5 до 10 в одном объявлении. Пропусков в значениях количества фотографий нету, но есть объявления с нулевым количеством фотографий. Количество объявлений без фотографий 1054, что составляет 0.45% от общего числа объявлений.
- Выяснили, что средняя цена в объявлениях около 6,5 млн. руб.
- Самые распространенные квартиры с площадью 45 кв.м.
- Наблюдаем также, что преобладают квартиры с высотой потолка 2.65 м.
- Самые распространённые кухни площадью от 5 до 15 кв.метров.
- Отметили по гистограмме значительное преобладание 5-этажных зданий. Наследие Хрущева. И 9-этажных зданий. Наследие Брежневских времён.
- Мы выяснили, что медианное время продажи - 95 дней
- Корреляция в 0.79 говорит о наличии связи между соотношщением стоимости квартир и их общей площади. Замечаем, что для квартир с небольшой общей площадью, значения стоимости квартир близко друг к другу. А вот для квартир элитного класса с большой площадью заметно значительное расхождение по стоимости квартиры в Санкт-Петербурге
- Заметили резкое снижение стоимости квартир начиная с 2014 года и только с 2017 года идет плавное увеличение стоимости, а значит и восстановление спроса
- Отметили слабую корреляцию между стоимостью 1 кв.м общей площади квартир и удаленностью от центра. Это связано с наличием дорогих элитных квартир по мере приближения к центру Санкт-Петербурга.
- Исследование показало, что самая дорогая стоимость 1 кв.м жилья в городе Зеленогорск, а не в Санкт-Петербурге. А Санкт-Петербург по стоимости уже идёт следом на 2 месте.
