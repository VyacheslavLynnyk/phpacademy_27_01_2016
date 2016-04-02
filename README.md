#Доманшняя робота на 06.04.2016

1. Переделать домашнюю работу описаную ниже в OOП парадигму
2. По возможности внедрить принцыпы SOLID
3. Выполнение заливать как ветку текущего репозитория с именем <username>_parice_oop. Ветку откалывать от коммита frist commit

1) Настройки подключения - перенести в отдельный файл, что-то типа config.inc.php и инклюдить его.

2) Максимально перенести код в функции. Также, куски кода могут быть похожи но отличаться переменными, параметрами, в общем - незначительно. Предусмотреть в функциях разное поведение в зависимости от параметров.

Например в index.php мы или добавляем новую запись или обновляем её. Переносим в функцию, которая реализует разный функционал в зависимости от полученных данных. Это как пример - так пересмотреть надо весь код.

3) Реализовать функцию для валидации данных из формы.

4) Пароль в базе хранить в md5+соль. Тогда в login.php надо изменить проверку пароля.

5) Добавить в базу поле для хранения даты изменения/добавления товара, и добавить в вывод.

6) В нашей реализации редактировать товары могут любые зарегестрированные юзеры. Это надо переделать. Добавить в логику поле role в таблице users. 

И тогда - если юзер_роль==1 (например) то он может редактировать товары. Если роль==0 то только просмотр. Реализация на ваше усмотрение, тут можно по-разному.

Задачи "Максимум".

1) У нас предусмотрено поле для хранения картинок товаров (image).

Реализовать логику для его обработки - добавить поле для загрузки файлов, и формировать поле image - как адрес где мы храним файл+его название(помним, что название лучше формировать самим). И тогда выводим эту картинку вместе с остальными полями.

2) Выводить для юзера - только товары которые есть в наличии(у нас предусмотрено это поле). Для админа - все товары.

3) У нас есть поле vendor. Реализовать возможность выбора производителей для вывода.

Аналогично, реализовать фильтр для выборки товаров - чтоб пользователь выбирал(в т.ч. сортировал) по цене - по уменьшению/увеличению, по алфавиту. 

А если не поленитесь пересобрать базу - то добавьте ещё таблицу категории, и в таблицу товаров дописать ключ - ид категории. Добавить возможность выбора категории для выборки. 

Реализовать возможность множественного фильтра, по всем вышеперечисленным параметрам.

Будет очень хорошо, если выборка будет визуально видна в адресной строке - user friendly url.

Что-то типа /?category=cardio&vendor=Gigaclub&priceorder=desc&price=200-500  - это как пример.*

