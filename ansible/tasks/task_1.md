# Ansible

- Перед выполнением заданий по репозиторию нужно пройти [хендбук по Python от Яндекс](https://education.yandex.ru/handbook/python) и только первые две главы + задачи. Если есть время и желание, то можно в фоне проходить и дальше, совмещая с прохождением курса.
- Читаем правила [Пункт 2](https://github.com/lamjob1993/linux-monitoring/blob/main/navigation/others/%D0%9F%D1%80%D0%B5%D0%B4%D0%B8%D1%81%D0%BB%D0%BE%D0%B2%D0%B8%D0%B5%20%D0%BA%20%D0%BA%D1%83%D1%80%D1%81%D1%83.md).

---

## Task 1

Для выполнения задач по всем разделам нам понадобится та же самая Ubuntu 22.04 + VPN, [как в репозитории Terraform](https://github.com/lamjob1993/terraform-monitoring/blob/main/terraform/tasks/task_1.md). Не забываем склонировать её перед использованием. 

### Пишем первую роль и деплоимся на x3 VM (эти машины оставляем для задания 1.1)

- Познакомьтесь с разделом [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/tree/main/ansible/tasks/monitoring_project):
  - Это рабочий проект **Ansible**.
  - У вас по следующим заданиям должен быть такой же.
- Самостоятельно выстройте логическую цепочку:
  - Откройте одновременно три файла (инвентори, плейбук и роль) в VS Code и самостоятельно проведите зависимости между файлами без помощи ИИ:
    - За что отвечают переменные.
    - Зачем нужен инвентори.
    - Какие модули задействуются.
    - Зачем нужен плейбук.
    - Зачем нужны роли.
- Установите **Ansible** на свободную VM из-под бинаря с официального сайта.
- Напишите и запустите роль **Process Exporter** сразу на трех VM по аналогии с разделом [monitoring_project](https://github.com/lamjob1993/ansible-monitoring/tree/main/ansible/tasks/monitoring_project):
  - **Process Exporter** ставим `Unit-файлом` со всеми вытекающими.
  - На VM должны стоять клиенты **openssh** - в большинство дистрибутивов клиенты встроенные.
- Проверьте с помощью скрипта **Ansible**, что **Process Exporter-ы** отдают метрики на `/metrics` и двигайтесь дальше.
- Запушьте изменения в **GitHub**.
