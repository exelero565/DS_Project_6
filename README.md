# PROJECT-6._Сегментация_клиентов_онлайн-магазина
<p align="center">
      <img src="https://github.com/exelero565/DS_Project_6/assets/97280394/a4a05833-eea2-4ba8-970d-0f3bbb7e158f" 
      width="300">
</p>

### Описание проекта
Построить модель кластеризации клиентов на основе их покупательской способности, частоты заказов и срока давности последней покупки, определить профиль каждого из кластеров.

### Краткая информация о данных
Данные представляют собой таблицу в формате CSV, в каждой строке которой содержится информация об уникальной транзакции.


**Основные цели проекта:**
- Произвести предобработку исходного набора данных о транзакциях.
- Провести разведывательный анализ данных и выявить основные закономерности.
- Сформировать набор данных о характеристиках каждого из уникальных клиентов.
- Построить несколько моделей машинного обучения, решающих задачу кластеризации клиентов, определить количество кластеров и проинтерпретировать их.
- Спроектировать процесс предсказания категории интересов клиента и протестировать вашу модель на новых клиентах.

### Метрика качества 
Для сегментирования - коэффициента силуэта, для классификации - точность (accuracy_score)

### Выводы:  
1 - Метод понижения размерности t-SNE справился лучше метода PCA. Это заметно на визуализациях:

- двухмерная - в одном случае (PCA) данные в куче, в другом (t-SNE) "карта" кластеров более разобщена на отдельные островки;
- полярная диаграмма кластеров - кластеры после пробразования методом t-SNE распределены равномерно в отличии от метода PCA, где разбиение кластеров почти незаметно (один огромный и еле заметный кластер);

2 - Алгоритм k-means++ показал наилучшие значения коэффициента силуэта среди трех моделей кластеризации. Модель AgglomerativeClustering была близка по результатам и определила на 1 кластер больше лидера. Модель GaussianMixture оказалась наименее подходящей для данного датасета.
  
  3 - Для предсказания кластеров алгоритм случайного леса справился качественнее и быстрее градиентного бустинга.

В целом, получилось преобразовать, подготовить, сегментировать данные, подобрать оптимальные гиперпараметры и создать RFM таблицу клиентов.
