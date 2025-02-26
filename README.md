# Домашнее задание к занятию «ELK»

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

---

## Дополнительные ресурсы

При выполнении задания используйте дополнительные ресурсы:
- [docker-compose elasticsearch + kibana](11-03/docker-compose.yaml);
- [поднимаем elk в docker](https://www.elastic.co/guide/en/elasticsearch/reference/7.17/docker.html);
- [поднимаем elk в docker с filebeat и docker-логами](https://www.sarulabs.com/post/5/2019-08-12/sending-docker-logs-to-elasticsearch-and-kibana-with-filebeat.html);
- [конфигурируем logstash](https://www.elastic.co/guide/en/logstash/7.17/configuration.html);
- [плагины filter для logstash](https://www.elastic.co/guide/en/logstash/current/filter-plugins.html);
- [конфигурируем filebeat](https://www.elastic.co/guide/en/beats/libbeat/5.3/config-file-format.html);
- [привязываем индексы из elastic в kibana](https://www.elastic.co/guide/en/kibana/7.17/index-patterns.html);
- [как просматривать логи в kibana](https://www.elastic.co/guide/en/kibana/current/discover.html);
- [решение ошибки increase vm.max_map_count elasticsearch](https://stackoverflow.com/questions/42889241/how-to-increase-vm-max-map-count).

**Примечание**: если у вас недоступны официальные образы, можете найти альтернативные варианты в DockerHub, например, [такой](https://hub.docker.com/layers/bitnami/elasticsearch/7.17.13/images/sha256-8084adf6fa1cf24368337d7f62292081db721f4f05dcb01561a7c7e66806cc41?context=explore).

### Задание 1. Elasticsearch 

Установите и запустите Elasticsearch, после чего поменяйте параметр cluster_name на случайный. 

*Приведите скриншот команды 'curl -X GET 'localhost:9200/_cluster/health?pretty', сделанной на сервере с установленным Elasticsearch. Где будет виден нестандартный cluster_name*.

---

### Задание 2. Kibana

Установите и запустите Kibana.

*Приведите скриншот интерфейса Kibana на странице http://<ip вашего сервера>:5601/app/dev_tools#/console, где будет выполнен запрос GET /_cluster/health?pretty*.

---

### Задание 3. Logstash

Установите и запустите Logstash и Nginx. С помощью Logstash отправьте access-лог Nginx в Elasticsearch. 

*Приведите скриншот интерфейса Kibana, на котором видны логи Nginx.*

---

### Задание 4. Filebeat. 

Установите и запустите Filebeat. Переключите поставку логов Nginx с Logstash на Filebeat. 

*Приведите скриншот интерфейса Kibana, на котором видны логи Nginx, которые были отправлены через Filebeat.*

![VirtualBox_Ubu2204_1_25_02_2025_18_27_04](https://github.com/user-attachments/assets/5ff08b13-af95-4533-ad5a-198c1399f976)
![VirtualBox_Ubu2204_1_25_02_2025_23_19_48](https://github.com/user-attachments/assets/d823f02c-4f47-49a1-a5fc-7381f1c2d6ad)
![VirtualBox_Ubu2204_1_25_02_2025_23_31_28](https://github.com/user-attachments/assets/bcb0197b-2624-4f20-93db-2cc12490914f)
![VirtualBox_Ubu2204_1_25_02_2025_23_36_14](https://github.com/user-attachments/assets/d73ba14f-9308-4c8e-b81e-7c62d6918788)
![VirtualBox_Ubu2204_1_25_02_2025_23_49_13](https://github.com/user-attachments/assets/ce4f2f90-770a-457f-8a1f-8ed7dfa58bf4)
![VirtualBox_Ubu2204_1_25_02_2025_23_53_49](https://github.com/user-attachments/assets/b2c0dff6-e38f-424b-bd50-040e7f33313d)
![VirtualBox_Ubu2204_1_26_02_2025_00_12_36](https://github.com/user-attachments/assets/ac7439bc-15ab-4a1a-8d2c-c18c340dd3c6)
![VirtualBox_Ubu2204_1_26_02_2025_03_04_02](https://github.com/user-attachments/assets/1eb9a075-b563-4fc9-86e3-aa2ae1186fcf)
![VirtualBox_Ubu2204_1_26_02_2025_03_32_05](https://github.com/user-attachments/assets/2a78a3bf-dd8d-4a80-b3ac-890b38884390)
![VirtualBox_Ubu2204_1_26_02_2025_03_37_22](https://github.com/user-attachments/assets/11bf295b-cd30-4fe3-880d-0cc1857461be)
![VirtualBox_Ubu2204_1_26_02_2025_03_45_40](https://github.com/user-attachments/assets/78f6b517-0ac9-438a-bc05-aef3ea47f0f5)


## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.

### Задание 5*. Доставка данных 

Настройте поставку лога в Elasticsearch через Logstash и Filebeat любого другого сервиса , но не Nginx. 
Для этого лог должен писаться на файловую систему, Logstash должен корректно его распарсить и разложить на поля. 

*Приведите скриншот интерфейса Kibana, на котором будет виден этот лог и напишите лог какого приложения отправляется.*
