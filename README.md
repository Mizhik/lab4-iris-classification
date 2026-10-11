# Лабораторна робота №4: класифікація ірисів

Реалізація прикладу **“A First Application: Classifying Iris Species”** з книги *Introduction to Machine Learning with Python* (сторінки PDF 27–38). Модель визначає вид ірису за чотирма вимірами чашолистків і пелюсток.

## Запуск

Потрібен Python 3.10 або новіший.

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter notebook iris_classification.ipynb
```

У Jupyter оберіть **Run All Cells**. Набір Iris завантажується через `scikit-learn`; окремо завантажувати дані не потрібно.

## Що робить Notebook

1. Завантажує 150 зразків Iris із чотирма числовими ознаками та трьома класами.
2. Перемішує дані й ділить їх на тренувальну (112) і тестову (38) частини з `random_state=0`.
3. Будує матрицю діаграм розсіювання для тренувальних даних.
4. Навчає `KNeighborsClassifier(n_neighbors=1)` лише на тренувальних даних.
5. Класифікує новий зразок `[5, 2.9, 1, 0.2]` як `setosa`.
6. Оцінює точність на відкладеному тестовому наборі: `0.9737` (37 правильних відповідей із 38).

Для сумісності з актуальними версіями pandas використано `pandas.plotting.scatter_matrix`, а для кольорів — стандартну палітру Matplotlib замість `mglearn`.
