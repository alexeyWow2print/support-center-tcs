---
title: Облачные диски
order: 6
---

# Облачные диски

## **Яндекс.Диск**

### Инструкция по интеграции Яндекс.Диск

Для создания приложения, перейдите по ссылке [https://oauth.yandex.ru/client/new](https://oauth.yandex.ru/client/new) &#x20;

Выберите платформу «Веб-сервисы» и введите Callback URL в формате [https://\*домен\*/api/cloudToken](https://elnar.tippo.ru/api/cloudToken)

<figure><img src="../../.gitbook/assets/Screenshot_2 (11).png" alt=""><figcaption></figcaption></figure>



Выберите доступы в **Яндекс.Диск REST API**:

* Доступ к информации о Диске
* Чтение всего Диска



<figure><img src="../../.gitbook/assets/Screenshot_2 (7).png" alt=""><figcaption></figcaption></figure>



Заполните поле «Ссылка на сайт» и сохраните изменения:

<figure><img src="../../.gitbook/assets/Screenshot_1 (31).png" alt=""><figcaption></figcaption></figure>



После создания приложения, выдаются все необходимые данные:

<figure><img src="../../.gitbook/assets/Screenshot_4 (6).png" alt=""><figcaption></figcaption></figure>



Перейдите в Админ-панель – Настройки – Интеграции – Яндекс.Диск. **Client ID** вставьте в поле ID, **Client secret** в поле Пароль и сохраните.

<figure><img src="../../.gitbook/assets/Screenshot_5 (7).png" alt=""><figcaption></figcaption></figure>



### Отображение на сайте

После прохождения интеграции в корзине доступна опция загрузки изображения из хранилища Яндекс.Диск

<figure><img src="../../.gitbook/assets/Screenshot_3 (9).png" alt=""><figcaption></figcaption></figure>



Отображаются файлы для выбора:

<figure><img src="../../.gitbook/assets/Screenshot_7 (11).png" alt=""><figcaption></figcaption></figure>







## Dropbox

### Инструкция по интеграции Dropbox

Зарегистрируйтесь на сервисе [https://www.dropbox.com/](https://www.dropbox.com/)

<figure><img src="../../.gitbook/assets/Screenshot_1 (12).png" alt=""><figcaption></figcaption></figure>



Перейдите в Личный кабинет – Профиль – Настройки – Apps - Просматривать файлы Dropbox - App Center

<figure><img src="../../.gitbook/assets/Screenshot_2 (12).png" alt=""><figcaption></figcaption></figure>



Нажмите на "Соберите приложение"

<figure><img src="../../.gitbook/assets/Screenshot_3 (12).png" alt=""><figcaption></figcaption></figure>



Создать приложения:

<figure><img src="../../.gitbook/assets/Screenshot_4 (18).png" alt=""><figcaption></figcaption></figure>



На следующем экране выберите пункты как на скрине ниже.

1. Выберите представленный вариант.
2. Выберите Full Dropbox – Access to all files and folders in a user's Dropbox.
3. Введите название для интеграции.

<figure><img src="../../.gitbook/assets/Screenshot_5 (10).png" alt=""><figcaption></figcaption></figure>



Откроется страница для заполнения:

В поле "URI перенаправления" введите данные в формате [https://\*домен\*/api/cloudToken](https://elnar.tippo.ru/api/cloudToken) и нажмите "Добавить"

В поле "Домены Chooser / Saver / Embedder" вставьте ссылку на ваш сайт

<figure><img src="../../.gitbook/assets/Screenshot_6 (18).png" alt=""><figcaption></figcaption></figure>



{% hint style="info" %}
Обратите внимание:

Пользователи разработки – Включить дополнительных пользователей можно до 500.
{% endhint %}

Далее во вкладке Разрешения отметьте нужные пункты и нажмите "Отправить":

<figure><img src="../../.gitbook/assets/Screenshot_7 (3).png" alt=""><figcaption></figcaption></figure>



Во вкладке Брендинг, вы сможете откорректировать Имя приложения, добавить описание, загрузить иконку.

<figure><img src="../../.gitbook/assets/Screenshot_8 (12).png" alt=""><figcaption></figcaption></figure>



Далее в Админ-панели сайта – Настройки – Интеграции – Облачные диски – Dropbox заполните данные App Key и App Secret из первой вкладки Приложения Dropbox и сохраните.

<figure><img src="../../.gitbook/assets/Screenshot_9 (2).png" alt=""><figcaption></figcaption></figure>



### Отображение на сайте



После прохождения интеграции в Корзине при загрузке файла будет доступна загрузка из аккаунта клиента на Dropbox. В корзине при первой загрузке, выйдет окно подтверждением

<figure><img src="../../.gitbook/assets/Screenshot_10 (3).png" alt=""><figcaption></figcaption></figure>



Разрешите

<figure><img src="../../.gitbook/assets/Screenshot_11 (5).png" alt=""><figcaption></figcaption></figure>

И у клиента при загрузке макета будет доступен вход в его аккаунт на Dropbox