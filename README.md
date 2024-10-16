# goit-algo-hw-06
## Тема 6. Графи

Перед початком роботи:
1. Версія **Python: >=3.10**
2. Cтворюємо віртуальне середовище (Python: >=3.10) `.env`: `python -m venv .env`
3. Активуємо (відповідно до своєї ОС): `source .env/bin/activate`
4. Інсталюємо залежності: `pip install -r requirements.txt`
5. По завершенню роботи деактивовуємо: `deactivate`

## Завдання 1
Створіть граф за допомогою бібліотеки `networkX` для моделювання певної реальної мережі (наприклад, транспортної мережі міста, соціальної мережі, інтернет-топології).
Візуалізуйте створений граф, проведіть аналіз основних характеристик (наприклад, кількість вершин та ребер, ступінь вершин).

### Критерії оцінювання:
- Створено та візуалізовано граф — модель певної реальної мережі.
- Проведено аналіз основних характеристик.

### Ресурси
- [task1.py](./task1.py)
- [graph_data.py](./graph_data.py)
- [Module helpers](./helpers)

## Завдання 2
Напишіть програму, яка використовує алгоритми `DFS` і `BFS` для знаходження шляхів у графі, який було розроблено у першому завданні.
Далі порівняйте результати виконання обох алгоритмів для цього графа, висвітлить різницю в отриманих шляхах. 
Поясніть, чому шляхи для алгоритмів саме такі.

### Критерії оцінювання:
- Програмно реалізовано алгоритми `DFS` і `BFS` для знаходження шляхів у графі, який було розроблено у першому завданні.
- Здійснено порівняння результатів алгоритмів для цього графа, пояснено різницю в отриманих шляхах. Обґрунтовано, чому шляхи для алгоритмів саме такі.
- Висновки оформлено у вигляді файлу `readme.md` домашнього завдання.

### Висновки
- `DFS` (Пошук у глибину):
  - Прагне якнайглибше проникнути в граф, перш ніж повернутися назад. 
  - Обирає один шлях і йде по ньому до кінця, перш ніж розглядати альтернативи. 
  - У нашому випадку, `DFS` може знайти довший шлях, але він буде першим повним шляхом, який алгоритм виявить.
- `BFS` (Пошук у ширину):
  - досліджує всі вершини на поточному рівні, перш ніж перейти на наступний рівень. 
  - Гарантовано знаходить найкоротший шлях у невзважених графах.
  - У нашому випадку, `BFS` знайде шлях з найменшою кількістю переходів між зупинками.

Різниця в отриманих шляхах:
- `DFS` може знайти довший шлях, який не обов'язково є оптимальним. Наприклад, він може пройти через більше зупинок, ніж потрібно.
- `BFS` завжди знаходить найкоротший шлях з точки зору кількості переходів. У нашому графі це означає маршрут з найменшою кількістю зупинок між початковою та кінцевою точками.

Причини різниці:
 - Стратегія пошуку: `DFS` "занурюється" глибоко в граф, тоді як `BFS` розширюється рівномірно у всіх напрямках.
 - Порядок відвідування: `DFS` може "застрягти" в довгому шляху, перш ніж розглянути коротші альтернативи. `BFS` розглядає всі коротші шляхи перед довшими.
 - Гарантії оптимальності: `BFS` гарантує найкоротший шлях у невзважених графах, `DFS` такої гарантії не дає.

У контексті транспортної мережі:
- `DFS` може імітувати маршрут, де людина просто йде вздовж першого доступного шляху, не зважаючи на ефективність.
- `BFS` більше схожий на те, як би людина планувала оптимальний маршрут, розглядаючи всі можливі варіанти на кожному етапі.

### Ресурси
- [task2.py](./task2.py)
- [graph_data.py](./graph_data.py)
- [Module helpers](./helpers)

## Завдання 3
Реалізуйте алгоритм Дейкстри для знаходження найкоротшого шляху в розробленому графі: додайте у граф ваги до ребер та знайдіть найкоротший шлях між всіма вершинами графа.

### Критерії оцінювання:
- У граф додано ваги ребер, програмно реалізовано алгоритм Дейкстри для знаходження найкоротшого шляху в розробленому графі.

### Ресурси
- [task3.py](./task3.py)
- [graph_data.py](./graph_data.py)
- [Module helpers](./helpers)

## Додатково
- [Домашнє завдання до теми "Графи"](https://www.edu.goit.global/uk/learn/24858703/19646173/19658290/homework)
- [https://github.com/nickolas-z/goit-algo-hw-06](https://github.com/nickolas-z/goit-algo-hw-06)
- [goit-algo-hw-06-main.zip](https://s3.eu-north-1.amazonaws.com/lms.goit.files/a9900e09-05ee-4b6b-8918-02235aab0b51%D0%94%D0%976_%D0%97%D1%83%D0%B1%D1%87%D0%B8%D0%BA%D0%9C%D0%B8%D0%BA%D0%BE%D0%BB%D0%B0%D0%9C%D0%B8%D0%BA%D0%BE%D0%BB%D0%B0%D0%B9%D0%BE%D0%B2%D0%B8%D1%87.zip)
- [Basic-Algorithms-and-Data-Structures-Neoversity](https://github.com/nickolas-z/Basic-Algorithms-and-Data-Structures-Neoversity)