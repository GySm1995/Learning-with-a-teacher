# Learning-with-a-teacher
YandexPraktikum Course - project 
# Описание проекта
 Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых. Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. 
 Данная задача относится к классу задач бинарной классификации. Алгоритмы, которые подходят для обучения модели: DT, LR, RF (DecisionTreeClassifier, LogisticRegression, RandomForestClassifier). Для построения модели и ее тестирования разобью данные на 3 выборки: обучающую, валидационную и тестовую в соотношении 6:2:2. Целевой признак - data_ohe['Exited'], остальное - нецелевые признаки признаки.
 # Основные этапы решения задачи
    1.  Загрузить и изучить файл с данными.
    2.  Исследовать баланс классов.
    3.  Выделить обущающую, валидационную и тестовую выборки из данных.
    4. Обучить модели без учёта дисбаланса классов. Сбалансировать классы и обучить модель, учитывая дисбаланс классов. 
    5. Выбрать лучшую модель. Проверить выбранную модель на тестовой выборке.
# Результат
    По результатам задачи можно сформулировать следующие выводы:
    1. Наилучшая модель согласно метрики f1-мера, это модель обученная алгоритмом случайного леса с гиперпараметрами max_depth=21, n_estimators=401, random_state=1.
    2. На тестовой выборке модель выдает следующий результат: f1-мера=0.624. (Точность модели 0.84, что выше константной модели для тестовой выборки, но этот параметр некорректен для сравнения в данной задачи).
    3. AUC-ROC лучшей модели случайного леса равен 0.86, т.е. модель на тестовой выборке 86% пар объектов классифицировала верно. В тестовой выборке классы не сбалансированы, поэтому оценка модели по параметру AUC-ROC является наиболее адекватной.
