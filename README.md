## Тестирование UI сайта компании "Т1 Консалтинг"
#### российский разработчик и интегратор, входит в Группу Т1
> <a target="_blank" href="https://www.t1-consulting.ru/">Ссылка на главную страницу сайта</a>


###  Содержание:

- [Технологии и инструменты]()
- [Технологии и инструменты](#earth_africa-технологии-и-инструменты)
- [Реализованные проверки](#earth_africa-Реализованные-проверки)
- [Сборка в Jenkins](#earth_africa-Jenkins-job)
- [Запуск из терминала](#earth_africa-Запуск-тестов-из-терминала)
- [Allure отчет](#earth_africa-Allure-отчет)
- [Отчет в Telegram](#earth_africa-Уведомление-в-Telegram-при-помощи-бота)
- [Видео примеры прохождения тестов](#earth_africa-Примеры-видео-о-прохождении-тестов)


### Проект реализован с использованием
IntelliJ IDEA Java Gradle Selenide Selenoid JUnit5 Jenkins Allure Report Allure TestOps Telegram Jira
<p align="center">
<img width="4%" title="IntelliJ IDEA" src="images/logo/Intelij_IDEA.svg">
<img width="4%" title="Java" src="images/logo/Java.svg">
<img width="4%" title="Selenide" src="images/logo/Selenide.svg">
<img width="4%" title="Selenoid" src="images/logo/Selenoid.svg">
<img width="4%" title="Allure Report" src="images/logo/Allure_Report.svg">
<img width="4%" title="Gradle" src="images/logo/Gradle.svg">
<img width="4%" title="JUnit5" src="images/logo/JUnit5.svg">
<img width="4%" title="GitHub" src="images/logo/GitHub.svg">
<img width="4%" title="Jenkins" src="images/logo/Jenkins.svg">
<img width="4%" title="Telegram" src="images/logo/Telegram.svg">
<img width="4%" title="Jira" src="images/logo/Jira.svg">
</p>

### Список проверок, реализованных в автотестах
- [x] Наличие  заголовка и меню на главной странице
- [x] Наличие заданных пунктов подменю в разделе "О компании" и проверка "девиза" компании
- [x] Проверка главного меню сайта с переменными названиями разделов меню, их наполнение страниц разделов
- [x] Проверка  меню и наполнение разделов меню "О компании"
  -    проверки проводятся с использованием параметризованных тестов
- [x] Проверка наличия и доступности к скачиванию инструкции по эксплуатации системы "T1 Watchman", формат PDF
  - проверка содержимого инструкции
- [x] Проверка на наличие ошибок в console log


### Сборка в Jenkins
### <img width="6%" title="Jenkins" src="images/logo/Jenkins.svg"> Запуск тестов в [Jenkins](https://jenkins.autotests.cloud/job/011_AlexGeorgievich_Home_13_v1/)
*Для запуска сборки необходимо указать значения параметров и нажать кнопку <code><strong>*Собрать с параметрами*</strong></code>.*

<p align="center">
  <img src="images/screens/Jenkins.png" alt="job" width="800">
</p>

<p align="center">
  <img src="images/screens/Jenkins2.png" alt="job" width="800">
</p>

### Удаленный запуск тестов

```bash
gradle clean test 
-Dbrowser=${BROWSER}
-DbrowserVersion=${BROWSER_VERSION}
-DbrowserSize=${BROWSER_SIZE}
-DremoteDriverUrl=https://${USER}:${PASSWORD}@${REMOTE_DRIVER_URL}/wd/hub/
-DvideoStorage=https://${REMOTE_DRIVER_URL}/video/
-Dthreads=${THREADS}
```
### Параметры сборки

> <code>BROWSER</code> – браузер, в котором будут выполняться тесты (_по умолчанию - <code>chrome</code>_).
>
> <code>BROWSER_VERSION</code> – версия браузера, в которой будут выполняться тесты (_по умолчанию - <code>91.0</code>_).
>
> <code>BROWSER_SIZE</code> – разрешени окна браузера, в котором будут выполняться тесты (_по умолчанию - <code>1920x1080</code>_).
>
> <code>REMOTE_URL</code> – адрес удаленного сервера, на котором будут запускаться тесты.
>
> <code>USER</code> - логин пользователя для подключения к Selenoid
>
> <code>PASSWORD</code> - пароль пользователя для подключения к Selenoid
>
> <code>THREADS</code> - количество одновременных запускаемых потоков для тестов.
>
 
### Запуск из терминала
```bash
gradle clean test
```
### Allure Reports отчет
### <img width="6%" title="Jenkins" src="images/logo/Jenkins.svg"> Запуск тестов в [Jenkins](https://jenkins.autotests.cloud/job/011_AlexGeorgievich_Home_13_v1/)
<p align="center">
  <img src="images/screens/AllureReport1.png" alt="job" width="800">
</p>

<p align="center">
  <img src="images/screens/AllureReport.png" alt="job" width="800">
</p>

### AllureTestOps отчет
### <img width="4%" title="Allure TestOPS" src="images/logo/Allure_Report.svg"> Интеграция с [Allure TestOps](https://allure.autotests.cloud/launch/11706)
<p align="center">
  <img src="images/screens/AllureTestOps.png" alt="job" width="800">
</p>

<p align="center">
  <img src="images/screens/AllureTestOps2.png" alt="job" width="800">
</p>

## Интеграция с Jira
 
### <img width="4%" title="Jira" src="images/logo/Jira.svg"> Интеграция с [Jira](https://jira.autotests.cloud/browse/AUTO-816)

<p align="center">
<img title="Jira issue" src="images/screens/jira.png">
</p>

### Отчет в Telegram

<p align="center">
  <img src="images/screens/telegram2.png" alt="job" width="400">
</p>

### Видео примеры прохождения тестов

> К каждому тесту в отчете прилагается видео.
<p align="center">
  <img title="Selenoid Video" src="images/screens/AllureReportVideo.mp4">
</p>
 

 
:heart: <a target="_blank" href="https://qa.guru">qa.guru</a><br/>
:blue_heart: <a target="_blank" href="https://t.me/qa_automation">t.me/qa_automation</a>
