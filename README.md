# vagrant-test

Необходимо:

- Запустить бокс "generic/ubuntu2004"
- С помощью Ansible:

  - Автоматически установить docker и docker-compose
  - Установить node exporter для Prometheus
  - Запустить 2 контейнера через compose файл:
  
    - С Prometheus, настроенным на сбор метрик с node exporter
    - С преднастроенной Grafana: datasource - Prometheus, + загружен 1860 dashboard

- Пробросить 3000 порт из контейнера в ВМ
- Пробросить 3000 порт из ВМ в хост

