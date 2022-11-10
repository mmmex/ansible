```
Ansible

Подготовить стенд на Vagrant как минимум с одним сервером. На этом сервере используя Ansible необходимо развернуть nginx со следующими условиями:

- необходимо использовать модуль yum/apt;
- конфигурационные файлы должны быть взяты из шаблона jinja2 с перемененными;
- после установки nginx должен быть в режиме enabled в systemd;
- должен быть использован notify для старта nginx после установки;
- сайт должен слушать на нестандартном порту - 8080, для этого использовать переменные в Ansible.

Критерии оценки:
Статус "Принято" ставится, если:

- предоставлен Vagrantfile и готовый playbook/роль (инструкция по запуску стенда, если посчитаете необходимым);
- после запуска стенда nginx доступен на порту 8080;
- при написании playbook/роли соблюдены перечисленные в задании условия.
```

* Клонируем проект: `git clone https://github.com/mmmex/systemd.git`

* Запускаем ВМ: `vagrant up`

Все необходимое будет выполнено автоматически скриптом `ansible`

Проверка: `curl localhost:8080`