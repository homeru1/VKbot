# pythonVkBot

## Плитки бота

### Новости
Делаем запрос GET запрос к https://api.nytimes.com/svc/topstories/v2/science.json?api-key={your-api-key} и получаем 100 последних новостей по рубрике "Наука".
Предварительно мы авторизировались на сайте NYT, чтобы получить "api-key" для выполнения GET-запроса. 
Запрос возвращает json объект, из которого пользователю выводим только 3 самые последние.

### Викторина
Ожидает начала викторины (нажатия кнопки "Старт"), после этого достает из файла с вопросами (questionsForQuiz.txt) случайный вопрос, которые ранее не задавался текущему пользователю, после этого проверяет кол-во ответов, если их >1, создает плитки с ответами. Далее получает ответ от пользователя и если он верный добавляет ему очков за правильный ответ. Задаваемые вопросы, счет и прочие переменные хранятся в структуре student.

## Формат файлов

### Викторина
Для работы викторины необходимо наличие файла "questionsForQuiz.txt". Структура данного файла: В первой строке пишется кол-во вопросов в файле, со второй строки идут уже сами вопросы в виде: 
\n№)"Вопрос""Ответ"
Вариант_1;Вариант_2;Вариант_3
Если вариант ответа всего один то ';' в конце ставить не нужно:
Вариант_1
