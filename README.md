# Анализ возраста

## Описание проекта
Сетевой супермаркет «Хлеб-Соль» внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:
* Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы;
* Контролировать добросовестность кассиров при продаже алкоголя.  

**Дано:** набор фотографий людей с указанием возраста.  
**Задача:** построить модель, которая по фотографии определит приблизительный возраст человека. 


## Было сделано
Исследованы возрастные рамки в данных. Проверено соответсвие фотографий и меток. Написаны функции для загрузки данных, создание модели и ее обучение. Использована архитектура  ResNet50.

## Вывод
Задачей было определить возраст по фотографии, добиться значение MAE меньше 7.
Построили модель с помощью архитектуры ResNet50, использовали оптимизатор Adam со скоростью обучения 0.001, в качестве функции потерь использовали среднеквадратическую ошибку. Оценивали качество с помощью метрики MAE. Получили результат на тестовой выборке 5.9 на 10 эпохе, что очень хорошо. Это значит, что наша модель в среднем ошибается меньше, чем на 6 лет. Но уже на 6 эпохе достигли необходимого результата - 6.77.
Итак, наша модель может хорошо подойти для анализа покупок и специализированных предложений в зависимости от возраста. Но для контроля продажи алкоголя модель не подойдет.
