# PR-2-HurzidzeAnton
## Хурцидзе Антон IПЗ 3.02 Практична робота № 2

## Тема: Комплексне дослідження структури, конфігурацій та робочого середовища сучасного JavaScript-проєкту на основі бойлерплейта vite-react-boilerplate
## Мета:
- Познайомитись із структурою файлу package.json як центрального конфігураційного файлу JavaScript-проєкту, зрозуміти основні поля: імʼя, автор, опис, версія, ліцензія, репозиторій, скрипти та залежності.
- Вивчити принципи семантичного версіонування (SemVer) через аналіз реальних залежностей.
- Ознайомитись із практикою оформлення проєктної документації (README.md).
- Вивчити призначення файлів .gitignore та LICENSE.
- Розібратися з роботою гіт-хуків через аналіз артефактів, які створює бібліотека Husky.

## Завдання 1.
1. Я склонував репозиторій vite-react-boilerplate використовуючи вiкно Clone Repository.

![1](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/1.png)
Рис. 1 - Вiкно Clone Repository

2. Я встановив усі залежності проєкту, використовуючи команду pnpm install.

![2](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/2.png)
Рис.2 - Робота команди pnpm install

3. Я запустив початковий скрипт сетапу проєкту (pnpm run setup).

![3](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/3.png)
Рис.3 - Робота команди pnpm run setup

## Завдання 2.
1. Опис призначення полів файлу package.json: name, author, description, version, license, repository, scripts, dependencies, devDependencies:
- Name - Назва проєкту, iдентифікатор проєкту в npm,
- Author - Контактна інформація розробника,
- Description - Короткий опис проєкту,
- Version - Семантична версія проєкту,
- License - Юридичні умови використання коду,
- Repository - Посилання на вихідний код,
- Scripts - Команди для автоматизації процесів,
- Dependencies - Бібліотеки, необхідні для роботи додатку,
- devDependencies - Інструменти розробки.
2. Аналізуйте залежності, вказані у dependencies та devDependencies, пояснення логіки такої класифікації:
- Dependencies включають бібліотеки, які безпосередньо необхідні для роботи додатку, а DevDependencies, натомість, складаються з інструментів, які потрібні лише під час розробки та не є частиною фінального коду.

## Завдання 3.
1. Я ознайомився із принципами SemVer.
2. Було зроблено версії пакетів бойлерплейту та зробленi пояснення які оновлення (мажорні, мінорні, патчі) допускаються відповідно до версій, зазначених у файлі package.json:

React-залежності:
- react: ^18.3.1 - дозволені всі версії 18.x, але не 19.x
- react-dom: ^18.3.1 - аналогічно React


Тестування та інструменти:
- @playwright/test: ^1.46.1 - всі версії 1.x, але не 2.x
- vitest: 2.0.5 - точно фіксована версія
- typescript: ^5.5.4 - всі версії 5.x, але не 6.x


Бібліотеки стану та маршрутизації:
- @tanstack/react-query: ^5.53.1 - всі версії 5.x
- @tanstack/react-router: ^1.51.6 - всі версії 1.x
- zustand: ^4.5.5 - всі версії 4.x

Devtools та розширення:
- @storybook/react: ^8.2.9 - всі версії 8.x
- eslint: ^9.9.1 - всі версії 9.x

## Завдання 4.
Я проаналізував та написав призначення, структуру та важливі елементи файлів:
Призначення:
README.md:
- Надає загальну інформацію про проект
- Пояснює, як встановити та запустити проект
- Документує доступні команди та залежності

.gitignore:
- Вказує Git, які файли та теки ігнорувати при відстеженні змін
- Запобігає випадковому комміту непотрібних файлів (залежності, логи, секрети)
- Зменшує розмір репозиторію
- Захищає чутливу інформацію

LICENSE:
- Визначає юридичні умови використання коду
- Захищає права автора
- Вказує, як інші можуть використовувати, змінювати та поширювати код
- Регулює взаємодію зopen-source спільнотою

Структура:
README.md:
- Назва проекту
- Короткий опис
- Встановлення
- Команди запуску
- Технології
- Налаштування

.gitignore:
- node_modules/
- dist/
- .env
- логи
- теки IDE
- тимчасові файли

LICENSE:
- Назва ліцензії (MIT)
- Копірайт
- Умови використання
- Відмова від відповідальності

## Завдання 5.
1. Я дослідив артефакти, які створюються після встановлення та налаштування бібліотеки Husky.
При встановленні Husky створюються .husky/pre-commit та .husky/commit-msg у теці .husky/, які містять службові скрипти для перевірки коду.

![4](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/4.png)

Рис.4 - Aртефакти при встановленнi Husky

3. Опиc, для чого потрібні ці артефакти, як вони налаштовуються та яку роль відіграють у процесі розробки:
Скрипти автоматично перевіряють код перед комітом, контролюють його якість, форматування, запускають лінтери та тести, валідують повідомлення комміту, забезпечуючи дотримання стандартів розробки безпосередньо в процесі роботи з репозиторієм.

## Завдання 6. 
1. Був написан скрипт, який читає довільну змінну оточення та друкує її значення у консоль:

![5](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/5.png)

Рис.5 - Скрипт env_variables.js

Виконавши команду node env_variables.js ми запустимо скрипт i побачимо результат:

![6](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/6.png)

Рис.6 - Помилка при вводi команди

Для уникнення данної помилки треба ввести команду встановлення бiблiотеки dotenv, а саме pnpm add dotenv:

![7](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/7.png)

Рис.7 - Встановлення бiблiотеки dotenv

Пiсля встановлення запускаємо скрипт:

![8](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/8.png)

Рис.8 - Правильна робота скрипта env_variables.js

2. Задавши різнi значення змінної оточення на різних рівнях (ОС, сесія терміналу, окремий запуск скрипта, dotEnv файл) я дослiдив пріоритетність їх застосування та
зафіксував отримані результати:

- Окремий запуск скрипта:

![9](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/9.png)

- Сесiя термiналу:

![10](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/10.png)

- На рiвнi ОС:

![11](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/11.png)

- Змiна в dotEnv файлi

![12](https://github.com/GAMECHl/PR-2-HurzidzeAnton/blob/main/12.png)

## Висновок

Виконана лабораторна робота дозволила глибше зрозуміти внутрішню структуру та налаштування сучасних JavaScript-проєктів. Були детально вивченi механізми конфігурації, версіонування та документування проєктів, що є ключовими навичками для ефективної front-end розробки. Отриманий досвід допоможе більш усвідомлено підходити до створення та підтримки складних веб-додатків.
