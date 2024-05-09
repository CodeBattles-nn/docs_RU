# Установка



## Docker

{% hint style="warning" %}
Если до этого у вас не был установлен Docker, пожалуйста, установите. Без этого ничего работать не будет [\[Ссылка на гайд по установке\]](https://docs.docker.com/engine/install/)
{% endhint %}

### Выберете вашу архитектуру

{% tabs %}
{% tab title="x64" %}
Для установки потребуется скачать репозиторий и развернуть Docker compose Container

скачивание образов из репозитория:

```bash
docker compose pull
```

запуск:

```sh
docker compose up
```


{% endtab %}

{% tab title="другие" %}
Для установки потребуется скачать репозиторий и развернуть Docker compose Container

сборка образов:

```bash
docker compose build
```

запуск:

```sh
docker compose up
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Для запуска контейнеров в фоновом режиме используйте флаг _<mark style="color:blue;">**-d**</mark>_

Пример:

{% code fullWidth="false" %}
```bash
docker compose up -d
```
{% endcode %}
{% endhint %}

После этого, пожалуйста, настройке языки программирования. Это описано на следующей странице
