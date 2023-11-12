# LR6
Лабораторная работа №6
### Система контроля версий

Цель лабораторной работы: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# ***Основная часть***

В репозитории создана папка screen, в которой хранятся все необходимые скриншоты.
Для наглядности проделанной работы была создана ветка lab6.

### ***Шаг один***
Создание аккаунта на GitHub или осуществления входа в существующий.

### ***Шаг два***
Копию репозитория в	личное	хранилище	из _https://github.com/Kurtyanik/LR6/_. Это осуществвляется с помощью _Fork_ (_См. screen/fork.PNG_). 

### ***Шаг три и шаг четыре***
Установка клиента Git, а затем его настройка - ввод ФИО и электронной почты. Данные задачи осуществляются с помощью _git config --global user.name_ и _git config --global user.email_ (_См. screen/name.PNG_).

### ***Шаг пять***
Далее необходимо клонировать свой личный удалённый репозиторий на компьютер. Клонирование происходит в папку lab6_, находящуюся на диске А (_См. screen/clone.PNG_).

### ***Шаг шесть***
Необходимо добавить	файл	через	интерфейс	GitHub и подтянуть	изменения	в локальный репозиторий. На скриншоте 3 (_См. screen/3.PNG_) представлены составляющие локального репозитория до обновленния данных и после. Поиск составляющих производится с помощью _ls -1_. Подтягивание информации осуществляется с помощью _git pull_

### ***Шаг семь и восемь***
Нужно получить историю операций для веток и просмотреть последние изменения. Узнать какие ветки существуют можно с помощью _git branch_, чтобы получить историю операций над ветками можно использовать _git reflog (имя ветки)_. Для просмотра последних изменений используется функция _log_ (_См. screen/4.PNG_)

### ***Шаг девять***
Следующим шагом необходимо выполнить	слияние	в	ветку	_master_. Слияние происходит из ветки Lab6_file. На скриншоте 6 (_См. screen/6.PNG_) видно, что содержимое Lab6_file_ добавилось в ветку _master_.

### ***Шаг десять***
Следующим шагом нужно удалить побочную ветку после успешного слияния. Делается это с помощью _git branch -d (имя ветки)_. В данном случае используется _git branch -d Lab6_file_ (_См. screen/6.PNG_).

### ***Шаг одиннадцать***
Для наглядной работы с репозиторием необходимо сделать изменения	и	зафиксировать	их,	оставляя	комментарии. Поочередно в репозиторий были добавлены три текстовых файла: _one_file.txt_, _two_file.txt_, _three_file.txt_. Что бы добавить изменения нужно воспользоваться _git add_, для создания коммита используется _git commit -m "(текст коммита)"_, для возвращения информации в репозиторий используется _git push_(_См. screen/7.PNG_).

### ***Шаг двенадцать***
Необходимо сделать откат коммита. Делается это с помощью _git revert HEAD --no-edit_( _См. screen/8.PNG_).
git config --global user.name "4216 Котелкина В.Д."

git config --global user.email "valeronk04@yandex.ru"

cd lab6_

git clone https://github.com/valeri2421/LR6.git

ls -1

cd LR6

ls - 1

git pull

ls -1

git reflog

git log

git checkout Lab6_file

ls -1

git checkout master

ls -1

git merge Lab6_file

ls -1

git branch -d Lab6_file

git add first.txt

git status

git commit -m "Первое изменение"

git push

git add second.txt

git status

git commit -m "Второе изменение"

git add second.txt

git status

git push

git commit -m "Третье изменение"

git push

git revert HEAD --no-edit

# ***История операций***
commit 9ac1ffbd04be77cd041c867cb2c249e6d0188f4c (HEAD -> lab6, master)
Author: 4216 Котелкина В.Д <valeronk04@yandex.ru>
Date:   Sun Nov 12 23:09:04 2023 +0300

    Revert "Третье изменение"

    This reverts commit 05a24b63cad1e08fc596983feb2a25ed2ee780a4.

diff --git a/three_file.txt b/three_file.txt
deleted file mode 100644
index 0128a34..0000000
--- a/three_file.txt
+++ /dev/null
@@ -1 +0,0 @@
-И здесь нет ничегоо
\ No newline at end of file

commit 05a24b63cad1e08fc596983feb2a25ed2ee780a4 (origin/master, origin/HEAD)
Author: 4216 Котелкина В.Д <valeronk04@yandex.ru>
Date:   Sun Nov 12 23:05:39 2023 +0300

    Третье изменение

diff --git a/three_file.txt b/three_file.txt
new file mode 100644
index 0000000..0128a34
--- /dev/null
+++ b/three_file.txt
@@ -0,0 +1 @@
+И здесь нет ничегоо
\ No newline at end of file

commit 4b863fb02baad47bd89956d6e081113d79dd51cf
Author: 4216 Котелкина В.Д <valeronk04@yandex.ru>
Date:   Sun Nov 12 23:04:50 2023 +0300

    Второе изменение

diff --git a/two_file.txt b/two_file.txt
new file mode 100644
index 0000000..711698b
--- /dev/null
+++ b/two_file.txt
@@ -0,0 +1 @@
+Здесь тоже нет ничего
\ No newline at end of file

commit 1696c51d8fbd9cbe506916d57cfbca91068643df
Author: 4216 Котелкина В.Д <valeronk04@yandex.ru>
Date:   Sun Nov 12 22:45:41 2023 +0300

    Первое изменение

diff --git a/one_file.txt b/one_file.txt
new file mode 100644
index 0000000..32c3131
--- /dev/null
+++ b/one_file.txt
@@ -0,0 +1 @@
+Здесь нет ничего
\ No newline at end of file

commit 4c25c289065890602bdea2a2fa428124774ed357
Author: Kotelkina Valeria <87972677+valeri2421@users.noreply.github.com>
Date:   Sun Nov 12 22:11:56 2023 +0300

    Create lab6_file

diff --git a/lab6_file.txt b/lab6_file.txt
new file mode 100644
index 0000000..e69de29

commit 921f53b8d0cebf542c791cf31f04e9b792f385a4
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:09:49 2020 +0300

    Обновление информации

diff --git a/mergefile.txt b/mergefile.txt
index 8b13789..6c1c959 100644
--- a/mergefile.txt
+++ b/mergefile.txt
@@ -1 +1,5 @@
-
+Файл
+заполнен
+очень
+важной
+информацией

commit c08a654a63cfc3a7146b2b7015884d9020f5cbf5
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:02:16 2020 +0300

    Файл создан пустым

diff --git a/mergefile.txt b/mergefile.txt
new file mode 100644
index 0000000..8b13789
--- /dev/null
+++ b/mergefile.txt
@@ -0,0 +1 @@
+

commit 3c6e9131bb47ed6009c28226afb0535c7f6d5964
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 19:58:20 2020 +0300

    Initial commit

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..8d912f2
--- /dev/null
+++ b/README.md
@@ -0,0 +1,2 @@
+# LR6
+Лабораторная работа №6
