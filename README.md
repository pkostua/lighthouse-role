lighthouse-role
=========

Эта роль скачиваeт и устанавливает статику lighthouse из https://codeload.github.com/VKCOM/lighthouse, устанавливает nginx для трансляции статики по http

Требования роли
-------------

- Ansible >= 2.7

Переменные роли
--------------

Вы можете переопределить vars переменные

| имя                   | область переопределения | значение по умолчанию                                              | описание                          |
|-----------------------|-------------------------|--------------------------------------------------------------------|-----------------------------------|
| lighthouse_static_url | vars                    | https://codeload.github.com/VKCOM/lighthouse/zip/refs/heads/master | адрес для скачивания статики      |
| lighthouse_static_dir | vars                    | /var/www/lighthouse                                                | место размещения статики на хосте |


Пример применения в Playbook
----------------

-Добавьте роль в зависимости вашего проекта

    - src: git@github.com:pkostua/lighthouse-role.git
      scm: git
      version: "0.0.0"
      name: lighthouse-role

-Добавьте запуск роли в playbook

    - hosts: servers
      roles:
         - lighthouse-role

### Источники

* [Lighthouse documentation](https://github.com/VKCOM/lighthouse)

