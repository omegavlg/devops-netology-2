# Домашнее задание к занятию "`Основы Git`" - `Дедюрин Денис`

Создаем репозиторий в GitLab (адрес: https://gitlab.com/omegavlg/devops-netology):
<img src = "img/01.png" width = 100%>

Переходим к репозиторию из прошлого задания и выполняем команды:
```
git remote -v
```
и
```
git remote add gitlab https://gitlab.com/omegavlg/devops-netology.git
```
<img src = "img/02.png" width = 100%>

После второго вызова команды git remote -v мы видим, что к уже существующему удаленному репозиторию origin, указывающему на GitHub, добавился новый удаленный репозиторий gitlab, указывающий на GitLab. Теперь у нас настроены два удаленных репозитория для одного локального проекта, и мы можем взаимодействовать с обоими.

Чтобы отправить изменения в новый удаленный репозиторий, выполняем команду:
```
git push -u gitlab main
```
<img src = "img/03.png" width = 100%>
<img src = "img/04.png" width = 100%>
<img src = "img/05.png" width = 100%>

Видим, что изменения опубликованы в GitLab.
<img src = "img/06.png" width = 100%>
