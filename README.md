## Restful Api on Flask

Данное приложение написано с использованием [Flask](http://flask.pocoo.org/) и базы данных [RethinkDB](https://www.rethinkdb.com/). Выбор [RethinkDB](https://ru.wikipedia.org/wiki/RethinkDB) обусловлен тем, что RethinkDB распределённая документоориентированная СУБД с открытым исходным кодом, сохраняющая данные в бессхемном JSON-формате. Ориентирована на применение для веб-приложений, требующих интенсивных обновлений базы данных.

Для работы с базой данных используется [диспетчер контекста](https://github.com/gwvsol/RethinkDB-context-manager) разработанный для этого приложения.

Описание развертывания приложения опробовано на [CentOS7](https://www.centos.org/).

Установка Python3

```shell
yum -y install yum-utils
yum -y groupinstall development
yum -y install https://centos7.iuscommunity.org/ius-release.rpm
yum -y install python36u
yum -y install python36u-devel
````
Устанаваливаем пакетный менеджер pip
```shell
yum -y install python36u-pip
#Обновляем pip
pip3.6 install --upgrade pip
```
