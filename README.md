<h1 align="center"> :boom: Проект по автоматизации тестирования WB </h1>

## :boom: Инструменты

<p  align="center"

<code><img width="5%" title="IntelliJ IDEA" src="images/IDEA-logo.svg"></code>
<code><img width="5%" title="Java" src="images/java-logo.svg"></code>
<code><img width="5%" title="Selenide" src="images/selenide-logo.svg"></code>
<code><img width="5%" title="Selenoid" src="images/selenoid-logo.svg"></code>
<code><img width="5%" title="Gradle" src="images/gradle-logo.svg "></code>
<code><img width="5%" title="JUnit5" src="images/junit5-logo.svg"></code>
<code><img width="5%" title="Allure Report" src="images/allure-Report-logo.svg"></code>
<code><img width="5%" title="Allure TestOps" src="images/allure-ee-logo.svg"></code>
<code><img width="5%" title="Github" src="images/git-logo.svg"></code>
<code><img width="5%" title="Jenkins" src="images/jenkins-logo.svg"></code>
<code><img width="5%" title="Jira" src="images/jira-logo.svg"></code>
<code><img width="5%" title="Telegram" src="images/Telegram.svg"></code>
</p>


### :boom: Реализованы проверки
#### - UI
 :heavy_check_mark: Поиск шапки через общее поле поиска 'Я ищу'

 :heavy_check_mark: Поиск джинс через общее поле поиска 'Я ищу'

 :heavy_check_mark: Проверка товаров в корзине

 :heavy_check_mark: Открытие раздела 'Доставка'

 :heavy_check_mark: Сообщение о проблеме

## :boom: Параметры запусков

For run remote tests need fill remote.properties or to pass value:

* browser (default chrome)
* browserVersion (default 89.0)
* browserSize (default 1920x1080)
* browserMobileView (mobile device name, for example iPhone X)
* remoteDriverUrl (url address from selenoid or grid)
* videoStorage (url address where you should get video)
* threads (number of threads)


Run tests with filled remote.properties:
```bash
gradle clean test
```

Run tests with not filled remote.properties:
```bash
gradle clean -DremoteDriverUrl=https://%s:%s@selenoid.autotests.cloud/wd/hub/ -DvideoStorage=https://selenoid.autotests.cloud/video/ -Dthreads=1 test
```

Serve report:
```bash
allure serve build/allure-results
```


###### For further development there are some example tests in src/test/java/cloud/autotests/tests/MainPageTest
* remove @Disabled("...") annotation to run tests
```bash
gradle clean test
```
## :boom: Результаты запусков
Параметры запуска в Jenkins
<p  align="left"
<code><img width="60%" title="Jenkins" src="images/paramzap.png"></code>
</p>
Отчёт о прохождении автотестов в Allure Report
<p  align="left"
<code><img width="60%" title="Allure Report" src="images/allurerep.png"></code>
</p>
Тест-кейсы в Allure TestOps
<p  align="left"
<code><img width="60%" title="Allure TestOps" src="images/tc.png"></code>
</p>
Интеграция с Jira
<p  align="left"
<code><img width="60%" title="Jira" src="images/jira.png"></code>
</p>
Пример запуска теста в Selenoid
<p  align="left"
<code><img width="60%" title="Selenoid" src="images/selenoid.gif"></code>
</p>
Уведомления о прохождении автотестов в Telegram
<p  align="left"
<code><img width="40%" title="Telegram" src="images/tg.png"></code>
</p>
