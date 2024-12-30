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

Редактируем файл README.md, добавляем директорию с картинками, тем самым переведя файл в состояние Modified.
<img src = "img/04.png" width = 100%>

Выполняем команду git diff, чтобы увидеть изменения
<img src = "img/05.png" width = 100%>

git add . и git status
<img src = "img/06.png" width = 100%>

Выполняем команду git diff --staged
<img src = "img/07.png" width = 100%>

Выполняем коммит
<img src = "img/08.png" width = 100%>

И снова git status
<img src = "img/09.png" width = 100%>

Выполняем команду git push, чтобы опубликовать все изменения.
<img src = "img/10.png" width = 100%>

Создадим файл .gitignore, выполним git add . и git status
<img src = "img/11.png" width = 100%>

Создадим директорию terraform и в ней так же разместим файл .gitignore с содержимым указанным в задании.
<img src = "img/12.png" width = 100%>
```
# Local .terraform directories
**/.terraform/*

# .tfstate files
*.tfstate
*.tfstate.*

# Crash log files
crash.log
crash.*.log

# Exclude all .tfvars files, which are likely to contain sensitive data, such as
# password, private keys, and other secrets. These should not be part of version 
# control as they are data points which are potentially sensitive and subject 
# to change depending on the environment.
*.tfvars
*.tfvars.json

# Ignore override files as they are usually used to override resources locally and so
# are not checked in
override.tf
override.tf.json
*_override.tf
*_override.tf.json

# Ignore transient lock info files created by terraform apply
.terraform.tfstate.lock.info

# Include override files you do wish to add to version control using negated pattern
# !example_override.tf

# Include tfplan files to ignore the plan output of command: terraform plan -out=tfplan
# example: *tfplan*

# Ignore CLI configuration files
.terraformrc
terraform.rc
```

В нем игнорируются следующие файлы и каталоги:

- Все файлы и папки внутри директорий .terraform (например, **/.terraform/*).
- Все файлы с расширением .tfstate и .tfstate.* (например, *.tfstate и *.tfstate.*).
- Все файлы с именем crash.log и все файлы с именем, начинающимся на crash. и заканчивающимся на .log (например, crash.log, crash.*.log).
- Все файлы с расширением .tfvars и .tfvars.json (например, *.tfvars, *.tfvars.json).
- Файлы с именем override.tf, override.tf.json, а также файлы, заканчивающиеся на _override.tf и _override.tf.json (например, override.tf, *_override.tf).
- Файл .terraform.tfstate.lock.info.
- Все файлы, начинающиеся с terraform.rc (например, .terraformrc, terraform.rc).

Эти файлы и каталоги обычно содержат конфиденциальную информацию, временные или специфичные для локальной среды данные, которые не следует отслеживать в системе контроля версий.

Создаем файлы will_be_deleted.txt (с текстом will_be_deleted) и will_be_moved.txt (с текстом will_be_moved) и коммитим их с комментарием Prepare to delete and move.
<img src = "img/13.png" width = 100%>

Удаляем файл will_be_deleted.txt из репозитория и переименовываем файл will_be_moved.txt в has_been_moved.txt. Коммитим полученные изменения.
<img src = "img/14.png" width = 100%>

Выведем git log
<img src = "img/15.png" width = 100%>