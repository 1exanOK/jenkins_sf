🛠️ CI/CD с Jenkins и Docker в Яндекс Облаке
📋 Задание
Реализован CI/CD-процесс с использованием Jenkins, развёрнутого на виртуальной машине в Яндекс Облаке.

☁️ Характеристики виртуальной машины:

Параметр	Значение
vCPU	2
RAM	2 GB
HDD	20 GB
ОС	Ubuntu 22.04
CI-сервер	Jenkins (в Docker)
Хостинг	Yandex Cloud
![image](https://github.com/user-attachments/assets/390a7e45-1e98-4653-a0fd-1035384ed41c)
![image](https://github.com/user-attachments/assets/bf193073-ad84-4945-9d0e-9c185f32a132)


🧪 CI/CD-процесс
🧱 Архитектура:
Git-репозиторий содержит файл index.html

Jenkins отслеживает изменения (через webhook или pull)

При изменении:

Собирается Docker-образ с nginx

Пробрасывается порт 9889:80

Копируется index.html

Выполняется проверка:

✅ HTTP-код должен быть 200

✅ md5-сумма ответа совпадает с оригиналом

В случае ошибки:

⚠️ Уведомление в Telegram

Контейнер удаляется
![image](https://github.com/user-attachments/assets/cb5bd09e-9707-41b8-a655-f0a7691787d8)


