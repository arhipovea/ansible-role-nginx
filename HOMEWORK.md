# Домашнее задание к занятию "09.04 Jenkins"

## Подготовка к выполнению

1. Создать 2 VM: для jenkins-master и jenkins-agent.
2. Установить jenkins при помощи playbook'a.
3. Запустить и проверить работоспособность.
4. Сделать первоначальную настройку.

## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.


![pic01](https://github.com/arhipovea/ansible-role-nginx/blob/master/assets/pic01.png)


2. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.

![pic02](https://github.com/arhipovea/ansible-role-nginx/blob/master/assets/pic02.png)

3. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.
4. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.

![pic03](https://github.com/arhipovea/ansible-role-nginx/blob/master/assets/pic03.png)

5. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).
6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True), по умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.

![pic04](https://github.com/arhipovea/ansible-role-nginx/blob/master/assets/pic04.png)

7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.
8. Отправить ссылку на репозиторий с [ролью](https://github.com/arhipovea/ansible-role-nginx) и [Declarative Pipeline](https://github.com/arhipovea/ansible-role-nginx/blob/master/Jenkinsfile) и [Scripted Pipeline](https://github.com/arhipovea/ansible-role-nginx/blob/master/ScriptedJenkinsfile).

---