

## Баг №1. Неверное сообщение при вводе корректных данных  
При вводе корректных данных на странице авторизации выводится неверное сообщение в неверном месте.  
**Серьезность:** Blocker  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. В поле `Username` ввести логин `admin`  
2. В поле `Password` ввести пароль `admin`  
3. Нажать на кнопку `Log in`  
**Ожидаемый результат:** Выводится сообщение `Logged In Successfully` 
**Фактический результат:** Выводится сообщение `Username not foundLog in successfull` 
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome  
  
## Баг №2. Неверное сообщение при верном логине и пустом пароле  
При вводе верного логина и незаполнении поля пароля выводится неверное сообщение в неверном месте.  
**Серьезность:** Trivial  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. В поле `Username` ввести логин `admin`  
2. Поле `Password` оставить пустым  
3. Нажать на кнопку `Log in`  
**Ожидаемый результат:** Выводится сообщение `Enter Both Username And Password`
**Фактический результат:** Выводится сообщение `Please enter bouth username and password`
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome  
  
## Баг №3. Неверное сообщение при пустом логине и верном пароле  
При незаполнении поля логина и вводе верного пароля выводится неверное сообщение в неверном месте.  
**Серьезность:** Trivial  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. Поле `Username` оставить пустым  
2. В поле `Password` ввести пароль `admin`  
3. Нажать на кнопку `Log in`  
**Ожидаемый результат:** Выводится сообщение `Enter Both Username And Password` 
**Фактический результат:** Выводится сообщение `Please enter bouth username and password`
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome  
  
## Баг №4. Неверное сообщение при верном логине и неверном пароле  
При вводе верного логина и неверного пароля выводится неверное сообщение в неверном месте.  
**Серьезность:** Major  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. В поле `Username` ввести логин `admin`  
2. В поле `Password` ввести пароль `qqq`  
3. Нажать на кнопку `Log in`  
**Ожидаемый результат:** Выводится сообщение `Incorrect password` 
**Фактический результат:** Выводится сообщение `Username not foundLog in successfull`
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome  
  
## Баг №5. Неверное сообщение при неверном логине и верном пароле  
При вводе неверного логина и верного пароля выводится неверное сообщение в неверном месте.  
**Серьезность:** Major  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. В поле `Username` ввести логин `admin`  
2. В поле `Password` ввести пароль `admin`  
3. Нажать на кнопку `Log in`  
**Ожидаемый результат:** Выводится сообщение `Username Not Found` 
**Фактический результат:** Выводится сообщение `Username not foundLog in successfull`
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome  
  
## Баг №6. Сброс языка при авторизации  
При смене языка и попытке авторизации язык сбрасывается  
**Серьезность:**  Minor  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. В поле `Username` ввести логин `admin`  
2. В поле `Password` ввести пароль `admin`  
3. Нажать на один из вариантов языка:  
- French  
- Italian  
- German  
4. Нажать на кнопку `Log in`  
**Ожидаемый результат:** Выбранный язык не сбрасывается после попытки авторизации  
**Фактический результат:** После смены языка на французский, итальянский, немецкий и авторизации, форма возвращается к английскому языку  
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome



## Баг №7. При переключении на немецкий или итальянский язык, кнопка log in отображается на французском языке

**Серьезность:**  Minor  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. Выбрать язык `Italian` или `German`

**Ожидаемый результат:** Кнопка `Log In`  переведется на итальянский или немецкий язык, в зависимости от выбора языка
**Фактический результат:** Кнопка `Log In` отображается на французском `S'identifier`
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome

## Баг №8.  Пустой логин и пароль не выдает никакого сообщения

**Серьезность:**  Minor  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. Поля Username и Password оставить пустыми
2. Нажать Log In

**Ожидаемый результат:**  Выводится сообщение `Enter Both Username And Password` 
**Фактический результат:** система никак не реагирует на нажатие кнопки
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome  

## Баг №9. Информационные сообщения выводятся в левом верхнем углу

**Серьезность:**  Minor  
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`  
**Шаги:**  
1. В поле `Username` ввести логин `admin`  
2. В поле `Password` ввести пароль `admin`  
3. Нажать на кнопку `Log in`  

**Ожидаемый результат:** Выводится сообщение `Logged In Successfully` над кнопкой `Log in`  
**Фактический результат:** Выводится сообщение `Username not foundLog in successfull` справа сверху страницы 


