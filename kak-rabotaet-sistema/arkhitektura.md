# Архитектура

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

_<mark style="color:red;">**Redis**</mark>_ - кеш для сложных запросов (...)

_<mark style="color:purple;">**Gateway**</mark>_ - Nginx для разделения запросов на несколько серверов

_<mark style="color:green;">**Init Configurer**</mark>_ - исполнение sql при первой загрузке приложения и инициализации стандартного состояния (Python)

_<mark style="color:blue;">**PostgeSQL**</mark>_ - база данных (...)

_<mark style="color:purple;">Frontend</mark>_ -Для интерфейса учителя  Nginx (JS, React)&#x20;

_<mark style="color:purple;">Frontend\_2</mark>_ -Для интерфейса участника Nginx (JS, React)

_<mark style="color:orange;">Backend</mark>_ - api (Python, Flask)

_<mark style="color:blue;">**\*\*\*\* cheker**</mark>_ - сервис для проверки задач на нужном языке (Java, Javalin)
