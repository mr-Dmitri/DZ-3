# Домашняя работа №3

## Задание

1. Выберите любой открытый датасет и скачайте открытый датасет, соответствующий вашим интересам или области обучения.
2. Создайте новую базу данных в системе управления базами данных (например, SQLite, PostgreSQL).
3. Создайте таблицу (или несколько таблиц) в базе данных с различными типами данных (INTEGER, TEXT, DATE), которые требуются для вашего датасета. Импортируйте данные из датасета в созданные таблицы.
4. Напишите несколько SQL-запросов для извлечения данных из таблиц базы данных. Используйте условия фильтрации (например, WHERE) для получения нужных данных.
5. Напишите SQL-запросы, использующие агрегатные функции (SUM, AVG, COUNT) для выполнения расчетов по данным таблицы.
6. Визуализируйте данные. Используйте библиотеки Python, такие как Matplotlib или Seaborn, для визуализации данных, извлеченных из базы данных. Постройте графики или диаграммы, которые помогут проанализировать и понять данные.

## Порядок запуска
1. Скачать файлы 
2. Установить зависимости: `pip install -r requirements.txt `
3. Создать каталог **"database"**, где будет храниться БД.
4. Запустить main.py

**_Примечания_**:<br>
* _Если нет Kaggle токена, тогда датасет необходимо скачать и разместить в папке **/dataset**._<br>
  _Чтобы не пришлось "танцевать с бубном" заранее разместил архив датасета в папке **/dataset** (это не правильно, но сделано во избежание "танцев")_
* _При выполнении скрипта будет создан каталог **/database**, в котором будет создан файл БД **"dataset.db"**._<br>
  _В БД загружаются данны датасета с разнесением некоторых данных в отдельные таблицы._ 

## Информация о датасете
Ссылка на датасет: https://www.kaggle.com/datasets/eduardolicea/healthcare-dataset/data<br>
Каждый столбец содержит конкретную информацию о пациенте, его поступлении и предоставляемых 
медицинских услугах, что делает этот набор данных подходящим для различных задач анализа данных 
и моделирования в области здравоохранения.

| №   | Столбец            | Значение                    | Пяснение                                                                                                                                                                                      |
|-----|--------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.  | Name               | Имя                         | В этом столбце указано имя пациента, связанное с медицинской картой.                                                                                                                          |
| 2.  | Age                | Возраст                     | Возраст пациента на момент поступления, выраженный в годах.                                                                                                                                   |
| 3.  | Gender             | Пол                         | Пол пациента: "Мужчина", "Женщина".                                                                                                                                                           |
| 4.  | Blood Type         | Группа крови                | Группа крови пациента, которая может быть одной из распространенных групп крови (например, "А+", "О-" и т.д.).                                                                                |
| 5.  | Medical Condition  | Медицинское состояние       | В этой колонке указывается основное медицинское состояние или диагноз, связанный с пациентом, например "Диабет", "Гипертония", "Астма" и другие.                                              |
| 6.  | Date of Admission  | Дата поступления            | Дата, в которую пациент был госпитализирован в медицинское учреждение.                                                                                                                        |
| 7.  | Doctor             | Врач                        | Имя врача, ответственного за уход за пациентом во время его поступления.                                                                                                                      |
| 8.  | Hospital           | Больница                    | Указывает медицинское учреждение или стационар, в который был госпитализирован пациент.                                                                                                       |
| 9.  | Insurance Provider | Поставщик услуг страхования | В этом столбце указывается поставщик услуг страхования пациента, который может быть одним из нескольких вариантов, включая "Aetna", "Blue Cross", "Cigna", "UnitedHealthcare" и "Medicare".   |
| 10. | Billing Amount     | Сумма счета                 | Сумма, на которую был выставлен счет за медицинские услуги пациента во время его госпитализации. Выражается в виде числа с плавающей запятой.                                                 |
| 11. | Room Number        | Номер палаты                | Номер палаты, в которой находился пациент во время его госпитализации.                                                                                                                        |
| 12. | Admission Type     | Тип приема                  | Определяет тип приема, который может быть "Экстренным", "Факультативным" или "Срочным", что отражает обстоятельства приема.                                                                   |
| 13. | Discharge Date     | Дата выписки                | Дата, в которую пациент был выписан из медицинского учреждения, основанная на дате поступления и случайном количестве дней в пределах реального диапазона.                                    |
| 14. | Medication         | Лекарственное средство      | Обозначает лекарственное средство, назначенное пациенту во время приема. В качестве примеров можно привести "Аспирин", "Ибупрофен", "Пенициллин", "Парацетамол" и "Липитор".                  |
| 15  | Test Results       | Результаты теста            | Описывает результаты медицинского обследования, проведенного при поступлении пациента. Возможные значения: "Нормальный", "Ненормальный" или "Неубедительный", указывающие на результат теста. |
| 16. | Length of Stay     | Продолжительность лечения   | Продолжительность лечения.                                                                                                                                                                    |

