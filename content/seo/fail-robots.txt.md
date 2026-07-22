---
title: Файл robots.txt
order: 1.9
---

## **Описание**

**Файл robots.txt** - это текстовый файл, который помогает владельцам сайтов сообщать поисковым роботам (ботам), какие страницы или разделы сайта можно просматривать и индексировать, а какие лучше не трогать.

**Основная цель файла robots.txt** -- указать поисковым роботам, какие страницы сайта не нужно показывать в результатах поиска. Например, это могут быть страницы для администраторов, копии других страниц или разделы, которые не должны быть доступны всем пользователям.

<figure>

![](<../../.gitbook/assets/image (251).png>)

<figcaption>



</figcaption>

</figure>

### **Структура файла**

Файл robots.txt состоит из набора правил, которые задаются для конкретных поисковых роботов (user-agent) или для всех ботов сразу. Основные директивы:

-  **User-agent**: указывает, для какого робота предназначено правило (например, `*` -- для всех роботов).

-  **Disallow**: запрещает доступ к указанным страницам или разделам.

-  **Allow**: разрешает доступ к определенным страницам, даже если они находятся в запрещенной директории.

-  **Clean-param**: команда, которая помогает поисковым роботам не путаться из-за лишних параметров в адресах страниц что бы не создать дубли.

## **Актуальный шаблон файла robots.txt** 

Вы можете **заменить текущий текст в файле robots.txt** на вариант, представленный ниже. Этот шаблон подойдет как для начального этапа, так и для дальнейшей работы с сайтом. При необходимости вы всегда сможете его отредактировать и адаптировать под свои задачи.



`User-agent: *` \
`Allow: /`

`Disallow: /assets` \
`Disallow: /order` \
`Disallow: /editor` \
`Disallow: /index.php/` \
`Disallow: /success` \
`Disallow: /fail` \
`Disallow: /afterEditor` \
`Disallow: /login` \
`Disallow: /registration` \
`Disallow: /recovery` \
`Disallow: /terms-of-use` \
`Disallow: /cookie` \
`Disallow: /design` \
`Disallow: /profile` \
`Disallow: /product/instruction`

`Disallow: /search` \
`Disallow: /backend`

`Clean-param: product_id` \
`Clean-param: utm_referer` \
`Clean-param: etext` \
`Clean-param: utm_ya_campaign` \
`Clean-param: utm_content` \
`Clean-param: utm_term` \
`Clean-param: yabizcmpgn` \
`Clean-param: utm_candidate` \
`Clean-param: utm_source` \
`Clean-param: utm_medium` \
`Clean-param: utm_campaign` \
`Clean-param: utm_content` \
`Clean-param: utm_term` \
`Clean-param: utm` \
`Clean-param: page`

`Sitemap: https://`<mark style="color:red;">`**ВАШ САЙТ**`</mark>`/sitemap.xml`



:::note 

Подробную информацию с рекомендациями по созданию/редактированию файла robots.txt можно изучить [здесь](https://developers.google.com/search/docs/advanced/robots/create-robots-txt?hl=ru).

:::