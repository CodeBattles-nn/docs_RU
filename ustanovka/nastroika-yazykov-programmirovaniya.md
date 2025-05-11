# Настройка языков программирования

## Добавление чекера языка программирования в базу данных

1. Запустить систему
2. Подключиться к базе данных _**cb**_(порт 25565)
3. Выбрать схему _**public**_
4. Выбрать таблицу _**servers**_
5. Внести данные (Добавить новый чекер)

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

6. Сохранить и закрыть.

{% hint style="info" %}
Для данных действий я использовал программу [_pgAdmin 4_](https://www.pgadmin.org/)
{% endhint %}

## Добавление других языков программирования в систему

Список подготовленных образов для языков программирования Вы можете найти [здесь](obrazy-chekerov.md).



* Скачайте _<mark style="color:purple;">**NAME**</mark>_.Dockefile (Где _<mark style="color:purple;">**NAME**</mark>_ - имя файла)
* В `docker-compose.yml` напишите новый сервис.\
  Пример нового `docker-compose.yml`\


<...> - сокращенный код

{% code title="docker-compose.yml" lineNumbers="true" %}
```yaml
version: "3.9"
services:
  frontend:
    build: FRONTEND/.
    ports:
      - "80:80"
    restart: unless-stopped
  <...>
  checker-goland:
    build:
      dockerfile: ./NAME.Dockerfile
    restart: unless-stopped

```
{% endcode %}

Более подробное описание файла:\
\
&#xNAN;_&#x421;трочка 3_ - системный сервис, где <mark style="color:red;">frontend</mark> - его название. Его трогать не нужно\
\
&#xNAN;_&#x421;трочка 9_ - наш новый чекер для языка программирования. Мы можем дать ему любое название, но я дам <mark style="color:red;">checker-goland</mark>\
\
&#xNAN;_&#x421;трока 10_: относительный путь до образа чекера\
(Кидать файл можно только в корень, путь - <mark style="color:red;">./</mark><mark style="color:purple;">NAME</mark><mark style="color:red;">.Dockerfile</mark>\


{% hint style="danger" %}
Внимание! В yml файлах отступы играют большую роль, поэтому копируйте, не забывая отступы
{% endhint %}

