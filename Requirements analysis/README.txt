1. Аналіз вимог
Опис задачі:
Навігація:

При натисканні на картку Do Your Workout на екрані Personal plan користувач має потрапляти до Trainings Tab.
Повна область картки є клікабельною та веде, при повторному натисканні, на екран Workout preview.
Блок "Today’s Activity" (на вкладці Trainings):

Відображається новий блок, що містить від 1 до 3 рекомендованих тренувань в залежності від кількості вибраних користувачем активностей.
Title: «Recommended for you».
Subtitle:
Якщо вибрано 1 активність:
"Get daily workouts tailored to your goal and interest in [Chosen Activity #1]."
(слово interest у однині)

Якщо вибрано 2 активності:
"Get daily workouts tailored to your goal and interests in [Chosen Activity #1] and [Chosen Activity #2]."

Якщо вибрано 3 активності:
"Get daily workouts tailored to your goal and interests in [Chosen Activity #1], [Chosen Activity #2] and [Chosen Activity #3]."

Оновлення Subtitle при виконанні тренувань (тільки якщо вибрано 2 і більше активностей):

Після виконання 1 тренування:
Subtitle змінюється на:
"Great job! [N] more workout left"
де N — кількість тренувань, що залишилися.

Після виконання всіх тренувань:
Subtitle змінюється на:
"All workouts done! For an extra challenge, check out the workout library below"

Інтеграція з існуючим функціоналом:

Після завершення всіх рекомендованих тренувань, на екрані Personal plan картка Do Your Workout має бути позначена як виконана.
Перехід на Workout preview screen повинен працювати коректно.
Результати Exploratory Testing (гіпотетично):
Перевірено, що після натискання на картку Do Your Workout користувач потрапляє на вкладку Trainings.
Блок Today’s Activity відображається з коректним Title та Subtitle, які залежать від кількості вибраних активностей.
Клікабельність картки перевірено: вся її область активна і веде до екрану Workout preview.
Тестовано відображення елементів при зміні орієнтації пристрою.
2. Тест кейси
TC1. Перехід з екрану Personal plan до Trainings Tab
Попередні умови:
Користувач знаходиться на екрані Personal plan.
Кроки:
Натиснути на картку Do Your Workout.
Очікуваний результат:
Користувач переходить до Trainings Tab, де відображається блок Today’s Activity.
TC2. Відображення блоку "Today’s Activity" для 1 обраної активності
Попередні умови:
У налаштуваннях/профілі користувача вибрано лише 1 активність ([Chosen Activity #1]).
Кроки:
Перейти на екран Personal plan.
Натиснути на картку Do Your Workout для переходу до Trainings Tab.
Очікуваний результат:
На вкладці Trainings у блоці Today’s Activity має відображатися:
Title: "Recommended for you"
Subtitle: "Get daily workouts tailored to your goal and interest in [Chosen Activity #1]."
TC3. Відображення блоку "Today’s Activity" для 2 обраних активностей
Попередні умови:
У профілі користувача вибрано 2 активності ([Chosen Activity #1] та [Chosen Activity #2]).
Кроки:
Перейти на екран Personal plan.
Натиснути на картку Do Your Workout.
Очікуваний результат:
У блоку Today’s Activity відображається:
Title: "Recommended for you"
Subtitle: "Get daily workouts tailored to your goal and interests in [Chosen Activity #1] and [Chosen Activity #2]."
TC4. Відображення блоку "Today’s Activity" для 3 обраних активностей
Попередні умови:
У профілі користувача вибрано 3 активності ([Chosen Activity #1], [Chosen Activity #2] та [Chosen Activity #3]).
Кроки:
Перейти на екран Personal plan.
Натиснути на картку Do Your Workout.
Очікуваний результат:
У блоку Today’s Activity відображається:
Title: "Recommended for you"
Subtitle: "Get daily workouts tailored to your goal and interests in [Chosen Activity #1], [Chosen Activity #2] and [Chosen Activity #3]."
TC5. Оновлення Subtitle після виконання однієї тренування (при 2 і більше активностях)
Попередні умови:
У профілі користувача вибрано 2 або більше активностей, відповідно відображається відповідна кількість рекомендованих тренувань.
Кроки:
На вкладці Trainings виконати одне з рекомендованих тренувань.
Очікуваний результат:
Після завершення однієї тренування, Subtitle змінюється на:
"Great job! [N] more workout left"
де N — кількість тренувань, що залишилися (наприклад, якщо було 2 тренування, то N = 1).

TC6. Оновлення Subtitle після виконання всіх рекомендованих тренувань
Попередні умови:
У профілі користувача вибрано 2 або більше активностей.
Кроки:
На вкладці Trainings виконати всі рекомендовані тренування.
Очікуваний результат:
Subtitle змінюється на:
"All workouts done! For an extra challenge, check out the workout library below"

TC7. Позначення картки "Do Your Workout" як виконаної на екрані Personal plan
Попередні умови:
Користувач завершив усі рекомендовані тренування.
Кроки:
Повернутися на екран Personal plan.
Очікуваний результат:
Картка Do Your Workout відображається як виконана (за графічною індикацією або позначкою статусу).
TC8. Перевірка клікабельності всієї області картки "Do Your Workout"
Попередні умови:
Користувач знаходиться на екрані Personal plan.
Кроки:
Натиснути на різні частини картки Do Your Workout.
Очікуваний результат:
Усі кліки ведуть до переходу на Workout preview screen.
Додаткові кейси для Exploratory Testing
TC9. Перевірка відображення блоку "Today’s Activity" при зміні орієнтації пристрою
Попередні умови:
Користувач знаходиться на вкладці Trainings з активним блоком Today’s Activity.
Кроки:
Змінити орієнтацію пристрою (з портретної на ландшафтну і навпаки).
Очікуваний результат:
Вміст блоку відображається коректно без накладань або втрати елементів.
TC10. Перевірка інтеграції нової функціональності з іншими екранами
Попередні умови:
Додаток знаходиться в робочому стані з активною новою фічею.
Кроки:
Навігація між екранами Personal plan, Trainings, та Workout preview.
Очікуваний результат:
Всі переходи відбуваються коректно, а інтеграція нової функціональності не впливає на інші частини додатка.