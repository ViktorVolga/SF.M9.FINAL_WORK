It is final work on module 9 from Skill Factory.
Multy users chat on windows terminal.

Многопользовательский чат.

Описание:
Содержит класс User, описанный в user.h в котором есть:

Приватные строки:
1. Имя.
2. Логин.
3. Пароль.

Методы:
1. getLogin() - получение логина.
2. getPass() - получение пароля

Содержит класс Message, описанный в message.h, в котором есть:

Приватные строки:
1. _from
2. _to;
3. _text;

Методы:
1. read - для чтения файлов 
2. getFrom - получение логина отправителя
3. get_To - получение логина получателя.

Содержит класс Chat, описанный в Chat.h, реализованный в Chat.cpp, в котором есть:

Векторы:
1. _users для хранения зарегестрированных пользователей.
2. _messages для хранения сообщений.

Указатели:
_currentUser - для индикации текущего залогиневшегося пользователя.

Переменные:
bool _chatWorking - true когда чат работает. 

Методы:
1. start - включает чат. 
2. menu - выводит пользователю меню предлагая залогиниться , зарегестрироваться или выйти.
3. login - запрашивает у пользователя логин и пароль.
Вызывает метод getUserByLogin который возвращает Уникальный указатель на User,
если указанный логин уже хранится в векторе _users. 
Если логин не найден генерирует исключение - класс Badlogin.
Исключение ловится и выводит на экран сообщение о том, что логин не зарегестрирован еще.
и присваивает указателю на текущего пользователя nullptr.
Вызывает метод chekUserPass - который проверяетправильность логина и пароля.
Если указан неправильный пароль - предлагает пользователю либо попробовать еще раз залогиниться,
или зарегестрироваться вызывая метод регистрации.
Если вектор _users пустой - вызывает метод registracion.
Если Логин и пароль правильные - вызывает пользовательское меню.
3. registracion. Запрашивает у пользователя Имя, Логин и Пароль. Вызывает конструктор класса User и
сохраняет пользователя в вектор _users.
Вов ремя регистрации проверяет занят ли логин методом getUserByLogin. Если пользователь есть
предлагает на выбор залогинится или взять другой логин.
4. getUserByLogin - берет переданный логин, "Пробегает" по вектору _users и в случае совпадения
переданного логина, уже сохраненному в векторе у пользователя - возвращает уникальный указатель на 
пользователя у которого совпал логин. Если логин не находится в векторе генерирует исключение.
5. userMenu - меню пользователя. Предлагает прочитать сообщение, написать сообщение и выйти.
Вызывая функции readMessages, createMessages, и присваивает _currentUser nullptr соответственно
в зависимости от выбора пользователя.
6. readMessages - пробегает по вектору _messages. В случае совпадения логина получателя и строки сообщения _to или если в строке _to указан получатель all - выводит сообщения на дисплей.
7. createMessage - запрашивает у пользователя кому он хочет отправить сообщение и текст сообщения.
Проверяет зарегестрирован ли логин получателя. Если нет - просит изменить получателя.
Если пользователь с указанным логином зарегестрирован или получатель all - 
вызывает конструктор класса Message. Сохраняет сообщение в вектор _messages.
8. checkLogin - принимает логин и проверяет вектор _users на наличие пользователя с таким логином.
Возвращает true если пользователь найден и false если пользователя нет.
9. chekUserPass - принимает логин и пароль и проверяет вектор _users на наличие пользователя 
с таким логином и паролем. Возвращает true если пользователь найден и false если пользователя нет.

Класс исключений Badlogin, описанный, в Chat.h в самом низу, который содержит:
1. Строку _login - которая хранит логин, который указан при попытке залогинится, но еще не зарегестрированный.
2. Функцию Show - которая выводит сообщение пользователю.

Мои контакты для связи:

dorodnikovviktor@gmail.com - временно не работает из-за ситтуации в мире. =(
dorodnikovviktor@yandex.ru - временный e-mail.

+7 (917) 169-30-72 - Телефон, Telegramm, What's app.

Открыт для сотрудничества.
Приму участие в любом проекте на С++.   
