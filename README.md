# rpm
Домашняя работа по теме управление пакетами и дистрибьюции софта

Для проверки дз, необходимо запутсить Vagrantfile.
Все необходимые операции по кстановки и настройке собсвенного репозитария
описаны в файле rpm.sh, который выполнится при запуске Vagrantfile.
Необходимо что rpm.sh и Vagranfile лежали в одной директории.
После того как виртуальная машина будет запущена , на ней необходимо выполнить
следующие команды для проверки собственного репозитория:

1. curl -a http://localhost/repo/ 

<html>
<head><title>Index of /repo/</title></head>
<body bgcolor="white">
<h1>Index of /repo/</h1><hr><pre><a href="../">../</a>
<a href="repodata/">repodata/</a>                                          20-Aug-2020 12:52                   -
<a href="nginx-1.14.1-1.el7_4.ngx.x86_64.rpm">nginx-1.14.1-1.el7_4.ngx.x86_64.rpm</a>                20-Aug-2020 12:51             2001440
<a href="percona-release-0.1-6.noarch.rpm">percona-release-0.1-6.noarch.rpm</a>                   13-Jun-2018 06:34               14520
</pre><hr></body>
</html>
Покажет что пакеты доступны


2. yum repoinfo otus

Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.reconn.ru
 * extras: mirror.sale-dedic.com
 * updates: mirror.sale-dedic.com
Repo-id      : otus
Repo-name    : otus-linux
Repo-status  : enabled
Repo-revision: 1597927920
Repo-updated : Thu Aug 20 12:52:00 2020
Repo-pkgs    : 2
Repo-size    : 1.9 M
Repo-baseurl : http://localhost/repo/
Repo-expire  : 21,600 second(s) (last: Thu Aug 20 12:52:01 2020)
  Filter     : read-only:present
Repo-filename: /etc/yum.repos.d/otus.repo

repolist: 2
Покажет инфу о собственном репо