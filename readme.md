### **Краткое описание работы с API**

Для подключения данной API требуется всего несколько действий:

- В файлы urlrewrite.php добавить правило;
- Добавить метод автозагрузки классов для работы с API (файл autoload.php);
- Подключить созданный/добавленный Autoloader в init.php;
- Скопировать директорию local/Api в проект (все метод задокументированы);
- В публичной части создать директории API к которой инициализировать App::call()->run();


Все методы максимально могут масштабироваться, дополняться, возможно применение любых паттернов программирования для более удобной работы и придерживания принципов ООП, SOLID.

### **Краткое описание**
- class Router для разбора полученного Request из Bitrix\Main\Context;
- class App для запуска MVC;
- class Autoload для загрузки всех классов API;

Все входящие параметры в классе Request уже проходят необходимую обработку со стороны Bitrix.
На вход могут поступать как GET, так и POST параметры.

### Примеры:

#### GET

- localhost/api/news/getNews/

###### С параметрами
- localhost/api/news/getNews/?id=324&text=test

#### POST

- localhost/api/news/getNews/
и в body сами параметры.

---------
#### Автозагрузку при желании можно заменить на автозагрузку composer.