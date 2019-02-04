## Restful Api on Flask

Данное приложение написано с использованием [Flask](http://flask.pocoo.org/) и базы данных [RethinkDB](https://www.rethinkdb.com/). Выбор [RethinkDB](https://ru.wikipedia.org/wiki/RethinkDB) обусловлен тем, что RethinkDB распределённая документоориентированная СУБД с открытым исходным кодом, сохраняющая данные в бессхемном JSON-формате. Ориентирована на применение для веб-приложений, требующих интенсивных обновлений базы данных.

Для работы с базой данных используется [диспетчер контекста](https://github.com/gwvsol/RethinkDB-context-manager) разработанный для этого приложения.

Описание развертывания приложения опробовано на [CentOS7](https://www.centos.org/).

Установка Python3

```shell
yum -y install yum-utils
yum -y groupinstall development
#Устанавливаем репозиторий Python3
yum -y install https://centos7.iuscommunity.org/ius-release.rpm
#Устанавливаем Python3
yum -y install python36u
yum -y install python36u-devel
#Устанаваливаем пакетный менеджер pip
yum -y install python36u-pip
#Обновляем pip
pip3.6 install --upgrade pip
#Устанавливаем репозиторий для установки базы данных RethinkDB
wget http://download.rethinkdb.com/centos/7/`uname -m`/rethinkdb.repo -O /etc/yum.repos.d/rethinkdb.repo
#Устанавливаем базу данных RethinkDB
yum install rethinkdb
```
Загрузка проекта и создание виртуальной среды 
```shell
mkdir webapp
cd webapp
git clone https://github.com/gwvsol/Restful-Api-on-Flask.git ./
python3.6 -m venv venv
#Активируем виртуальную среду
source venv/bin/activate
#Обновляем pip3
pip3 install --upgrade pip
#Установливаем зависсимости
pip3 install -r requirements.txt
```
