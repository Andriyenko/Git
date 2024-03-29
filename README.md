# Работа с git 

Знакомство с распределенной системой управления версиями

## С него начать?

Git (произносится «гит»[10]) — распределённая система управления версиями. Проект был создан Линусом Торвальдсом для управления разработкой ядра Linux, первая версия выпущена 7 апреля 2005 года. На сегодняшний день его поддерживает Джунио Хамано.

## Список основных команд для работы с git
Инициализация локального репозитория
```
git init
```
Первое, что вам следует сделать после установки Git — указать ваше имя и адрес электронной почты, к примеру(имя, фамилия, редактор):
```
git config --global core.editor "vim"
git config --global user.name "Vladimir Andriyenko"
git config --global user.email andriyenko@live.ru
```
Промотр внесенных изменений:
```
git config --list
```
Добавление удаленного репозитория:
```
git remote add rebrain https://localhost
```
Просмотр удланных репозиториев:
```
git remote -v
```
Вносим изменения, добавляем новые файлы в коммит, проверяем статус, добавляем коммит, отправляем изменнения на удаленный репозиторий, перезапись удаленного репозитория при конфликтах:
```
git add -A
git status
git commit -a -m "Добавляем файл readme.md в репозиторий"
git push удаленный репозиторий ветка
git push --force репозиторий ветка
```
Добавляние метки к коммиту, пушим изменения, просмотр изменений:
```
git tag -a v0.1 хэш коммита
git push --tags
git show v0.1
```
Создание ветки и переключиться в новую ветку:
``` 
git checkout -b style
```
Переключение между коммитами, ветками:
```
git checkout (название ветки или хэш коммита)
```
Просмотр веток, удаление:
```
git branch
git branch -d название ветки
```
Слияние веток:
Документация по ветвлению и слиянию * [Git](https://git-scm.com/book/ru/v2/%D0%92%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B2-Git-%D0%9E-%D0%B2%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B8-%D0%B2-%D0%B4%D0%B2%D1%83%D1%85-%D1%81%D0%BB%D0%BE%D0%B2%D0%B0%D1%85)
Основное отличие git merge от git rebase, rebase линейная история без лишних коммитов, полная история коммитов - megre.
```
git merge название веток
git rebase название веток
```
Откат изменений на определенный коммит:
```
git reset --hard хэш коммита (после данного коммита изменения будут утеряны)
```
Применение одного коммита из другой ветки:
```
git cherry-pick хэш коммита
```
Переименивание последнего коммита:
```
git commit --amend -m
```
Просмотр истории коммитов, журнал ссылок,, историю изменения файла
```
git log
git diff название файла
git reflog 
git blame название файла
```

## Полезное
* Статья на habr, как писать коммиты: [habr](https://habr.com/ru/post/416887/)
* Markdown - это легкий и простой в использовании синтаксис для стилизации: [Markdown](https://guides.github.com/features/mastering-markdown/)
* Темплейт шаблона md файла: [Template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2)
* Онлайн-сервис для генерации gitignore в разных ситуациях [gitignore](https://www.gitignore.io/)
* Визуализация слияния веток [Визуализация веток](https://learngitbranching.js.org)
* Безболезненное разрешение Merge конфликтов в [Git](https://habr.com/ru/post/323234/)

## Оф. документация

* [Git](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%9E-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B5-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8F-%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9) - документация
