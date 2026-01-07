# Telco-Customer-Churn-Prediction-using-Tree-Based-Methods

Описание проекта

Данный проект представляет собой комплексный анализ данных телеком-компании с целью построения моделей для предсказания оттока клиентов (Churn). Используется датасет `Telco-Customer-Churn.csv` с информацией о 7032 клиентах и 21 признаком [file:53].

## Основные этапы работы

### 1. Exploratory Data Analysis (EDA)
- Загрузка и первичный анализ данных 
- Статистический анализ численных и категориальных признаков 
- Визуализация распределений 

### 2. Cohort Analysis
Анализ когорт по параметру `tenure` показал 
- Для tenure = 1 месяц: **churn rate = 61.99%** 
- Для tenure = 72 месяца: **churn rate = 1.66%** 
- Четкая обратная зависимость между длительностью обслуживания и оттоком 
### 3. Feature Engineering
- Создание признака `Tenure Cohort` для группировки клиентов 
- Преобразование категориальных признаков 

### 4. Machine Learning Models

Реализованы и протестированы следующие модели 

| Модель | Accuracy | Precision (Churn) | Recall (Churn) | F1-Score (Churn) |
|--------|----------|-------------------|----------------|------------------|
| Decision Tree (max_depth=6) | 0.81 | 0.55 | 0.49 | 0.52 |
| Random Forest | 0.80 | 0.51 | 0.43 | 0.47 |
| AdaBoost | 0.83 | 0.60 | 0.51 | 0.55 |
| Gradient Boosting | 0.82 | 0.57 | 0.50 | 0.53 |

### 5. Model Evaluation
- Classification Reports для всех моделей
- Confusion Matrix визуализация с использованием `ConfusionMatrixDisplay` 
- Feature Importance Analysis для Decision Tree 

##  Технологический стек

- Python 3.x
- pandas, numpy - обработка данных
- matplotlib, seaborn - визуализация
- scikit-learn - машинное обучение:
  - DecisionTreeClassifier
  - RandomForestClassifier
  - AdaBoostClassifier
  - GradientBoostingClassifier
 
Ключевые выводы
Лучшая модель: AdaBoost показал лучшую accuracy (0.83) и баланс метрик 
Проблема классового дисбаланса: Все модели лучше предсказывают класс "No Churn" (support=557) vs "Yes Churn" (support=147) 
Feature Importance: Визуализация показала наиболее значимые признаки для предсказания оттока 
