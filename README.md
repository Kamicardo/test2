# test2
Виртуальная машина создана через Hyper-V
CentOS 7 в минимальной конфигурации
Для начала обновил текущий репозиторий 
	yum -y update
Далее добавил дополнительный репозиторий EPEL 
	yum install -y epel-release
Далее установка nginx
	yum –y install nginx
Настройка автоматического запуска сервиса
	systemctl enable nginx
Непосредственно запуск
	systemctl start nginx
Проверка работы сервиса
	systemctl status nginx
Открытие портов в фаерволе
	firewall-cmd --zone=public --permanent --add-service=http
	firewall-cmd --zone=public --permanent --add-service=https
	firewall-cmd --reload
Определение текущего адреса машины
	ip a
Файл настроек nginx размещен в /etc/nginx/conf.d/ (скопирован в проект как test.conf)
Александр помог с сетевыми настройками для возможности доступа в машине извне (адрес динамический, если необходимо проверить работу nginx - текущий адрес уточнить у меня)

Так же установлен ansible и gnome gui для работы с pycharm
В проекте наработки по роли установки nginx, но сделаны опять же при помощи Александра, принцип работы с ansible понял, но нужно разбираться с синтаксисом (очень мало опыта работы с linux в целом и centos в частности)
