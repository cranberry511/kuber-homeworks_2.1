## Решение задания 1

Создание Deployment приложения, состоящего из двух контейнеров, обменивающихся данными:
https://github.com/cranberry511/kuber-homeworks_2.1/blob/main/containers-data-exchange.yaml
![Deployment](img/getpod1.jpg)

Описание пода с контейнерами:  
![Describe](img/describe.jpg)

Вывод команды чтения файла:
![tail](img/tail.jpg)


## Решение задания 2

Создание Deployment приложения, использующего локальный PV, созданного вручную:
https://github.com/cranberry511/kuber-homeworks_2.1/blob/main/pv-pvc.yaml
![Deployment2](img/getpod2.jpg)

Удаление Deployment и PVC:
![After delete](img/after_delete.jpg)

Убеждаемся, что файл сохранился на локальном диске ноды:
![File exist](img/file_exist.jpg)

Данное поведение объясняется значением параметра persistentVolumeReclaimPolicy: Retain, содержимое тома сохраняется после удаления PVC и Deployment, статус меняется на Released

Удаление PV:
![PV delete](img/pv_delete.jpg)

Проверяем, что произошло с файлом после удаления PV:
![PV exist](img/pv_exist.jpg)

Файл остался также из-за параметра persistentVolumeReclaimPolicy: Retain


## Решение задания 3

Создание Deployment приложения, использующего PVC, созданный на основе StorageClass:
https://github.com/cranberry511/kuber-homeworks_2.1/blob/main/sc.yaml
![StorageClass](img/sc.jpg)