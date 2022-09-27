HELLO

СОЗДАТЬ ЛОКАЛЬНЫЙ РЕПОЗИТОРИЙ
1) правой кнопкой по папке которую публикуем = Git Bash here
при открытии должен высветиться путь
2) проверяем имя 
 git config --dlobal user.name (если нет задаем  git config --dlobal user.name "Имя")
3) проверяем почту
 git config --dlobal user.email (если нет задаем  git config --dlobal user.email "Почта")
4) инициализируем
git init
создается ветка (master)
5) проверяем статус
 git status
=
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Form1.cs
        README.txt

nothing added to commit but untracked files present (use "git add" to track)

видит файлы, но они не добавлены
6) добавляем файлы перечислением
git add Form1.cs README.txt
7) проверяем
git status
=
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Form1.cs
        new file:   README.txt

добавлись
это первые добавленные изменения
8) зафиксировать изминения
$ git commit -m 'Firs commit' (где -m 'комментарий')
=
появился Первый коммит
$ git commit -m 'Firs commit'
[master (root-commit) b065987] Firs commit
 2 files changed, 4 insertions(+)
 create mode 100644 Form1.cs
 create mode 100644 README.txt

9) просмотрим историю изменений
git log
=
$ git log
commit b06598738027eda7e10b08a03709ca189ea68c10 (HEAD -> master)
Author: Angelika Stepanova <74lika1984@gmail.com>
Date:   Tue Sep 27 23:22:20 2022 +0300

    Firs commit

видно кто сделал комит - автора, время и комментарий
b06598738027eda7e10b08a03709ca189ea68c10 - это хеш комита,
по которому с этим комитом можно взаимодействовать (перейти, скопировать на другую ветку)

10) если что-то поменяли Git сразу видит
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.txt

no changes added to commit (use "git add" and/or "git commit -a")

11) его тоже добавляем
git add README.txt
enter
git commit -m 'modified README'

***************