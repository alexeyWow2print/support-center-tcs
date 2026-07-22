---
title: Общие настройки
order: 0.5
---

## **Теги robots (noindex, nofollow)**

:::info 

Все страницы сайта по умолчанию имеют метатеги index и follow

:::



Данный параметр открывает возможность добавлять теги noindex и nofollow в настройки каждой страницы сайта.

![](<../../.gitbook/assets/image (2222).png>)



В коде страницы они имеют следующий вид:

```
<meta name="robots" content="noindex, nofollow" />
```

#### Что это за метатеги и для чего они нужны. 

Варианты использования:

-  \<meta name="robots" content="**noindex**, **follow**" />\
   Нужно использовать в случае, если вы не хотите, чтобы страница была проиндексирована поисковыми системами, но роботы смогли бы перейти по ссылкам с этой страницы на другие.

-  \<meta name="robots" content="**noindex**, **nofollow**" />\
   Запрещает индексировать контент на соответствующей странице, а также запрещает роботам переходить по ссылкам.

-  \<meta name="robots" content="**index**, **follow**" />\
   Разрешает роботам индексировать страницу и переходить по ссылкам.

-  \<meta name="robots" content="**index**, **nofollow**" />\
   Разрешает индексировать страницу, но по ссылкам, которые в ней содержатся, робот переходить не будет.





## **Указывать у страниц каноническую ссылку на саму себя**

В настройках каждой страницы сайта имеется поле Canonical link.

Каноническая ссылка -- это ссылка, которая указывает на каноническую (предпочитаемую) страницу в группе схожих по содержимому страниц. Проще говоря канонический URL страницы -- это адрес, который будет индексироваться при наличии страниц-дублей.

![](<../../.gitbook/assets/image (2222).png>)

В коде страницы имеет следующий вид:

```
<link rel="canonical" href="https://demo.wow2print.com"/>
```





## **Ежедневное автоматическое обновление карты сайта**

При создании новых страниц, необходимо обновлять карту сайта. Ежедневное автоматическое обновление карты сайта полезно на старте, когда активно создаются новые стандартные страницы и страницы с продукцией. В дальнейшем эту функцию можно отключить. Также данный параметр необходим в том случае, если вы активно ведете блог или регулярно пополняете статьи на сайте.

Данный параметр является необязательным, он позволяет включить автоматическое обновление карты сайта на ежедневной основе.

Подробнее о карте сайта можно узнать в соответствующем разделе - [карта сайта](./_index#karta-saita-sitemap).





## **Карта сайта -- тег priority**

Поисковые роботы Яндекса и Гугла заходят на сайт и «гуляют» по нему какое-то время. Объем страниц, которые робот может изучить за определенный период времени ограничен, чтобы не задерживать робота и в то же время улучшить индексацию сайта, можно выставить на страницы приоритет.\
Тег показывает, какие страницы нужно проиндексировать как можно скорее, то есть данный тег расставляет приоритет важности (очередь на индексирование). Значение задаётся от 0.0 до 1.0, значение для всех страниц по умолчанию равно 0.5 (главная страница -- 1.0).\
Данный тег является необязательным, он лишь позволяет добавить страницам в карте сайта определенный приоритет.

В карте сайта данный тег выглядит следующим образом:

```
<url>
<loc>https://demo.wow2print.com</loc>
<priority>1.0</priority>
</url>
```



Информация о теге priority отобразится в файле карты сайта (sitemap.xml) только после его обновления.

:::info 

Приоритет -- это относительная величина, поэтому нет смысла писать для всех страниц (с целью накрутки) приоритет – 1.0, это ни к чему не приведет.

Приоритет -- не влияет на позиции страниц в поисковой выдаче. Его значение влияет только на очередь индексирования между страницами вашего сайта.

:::





## **Микроразметка schema.org**

Микроразметка schema.org позволяет структурировать данные страницы.\
Ее использование гарантирует, что поисковой робот извлечет информацию с сайта правильно. Для этого schema.org использует систему тегов.

Для разного типа контента schema предусматривает соответствующие теги.

:::info 

Следующие *теги* используются на странице «Продукции»

:::



-  **Тип PRODUCT**

   -  name (наименование продукта). Данные берутся из раздела SEO в продукции, параметр Title.

   -  description (описание продукта). Данные берутся из раздела SEO в продукции, параметр Description.

   -  image (изображение продукта)

   -  brand (наименование типографии)

   -  sku. Данные берутся из параметра «Артикул продукта»



#### Пример микро-разметки:

```
<div itemscope itemtype="http://schema.org/Product">
    <meta itemprop="name" content="Буклеты «Евро»"/>
    <meta itemprop="description" content="Буклеты «Евро»"/>
    <meta itemprop="image" content="/uploads/storageCache/2177/store/product/72956824960c0e11e27b1e5.33672490.jpg"/>
    <meta itemprop="brand" content="ООО «Ваша Типография»"/>
    <meta itemprop="sku" content="DW2P-036-2021"/>
</div>
```



-  **Тип OFFERS**

   -  url (ссылка на продукт)

   -  PriceCurrency (валюта)

   -  Price (цена)

   -  EligibleQuantity (тираж)

   -  Availability (наличие продукции)



#### Пример микро-разметки:

```
<div itemprop="offers" itemscope itemtype="http://schema.org/Offer">
        <meta itemprop="priceCurrency" content="RUB"/>
        <meta itemprop="price" content="4990"/>
        <meta itemprop="EligibleQuantity" content="100"/>
        <link itemprop="availability" href="http://schema.org/InStock"/>
        <link itemprop="url" href="https://demo.wow2print.com/produkciya/buklety-evro.html"/>
</div>
```



:::info 

Следующая *микро-разметка* используются для хлебных крошек

:::

#### Пример:

```
<div class="container container-breadcrumb">
	<ul class="breadcrumb" itemscope itemtype="https://schema.org/BreadcrumbList">
		<li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
			<a itemprop="item" href="/">
			<span itemprop="name">Главная</span></a>
			<meta itemprop="position" content="1" />
		</li>
		<li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
			<a itemprop="item" href="/vse-buklety">
			<span itemprop="name">Буклеты</span></a>
			<meta itemprop="position" content="2" />
		</li>
		<li class="active" itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem"><span itemprop="name">Буклеты «Евро»</span>
		<meta itemprop="position" content="1" />
		</li>
	</ul>
</div>
```



:::info 

Следующая *микро-разметка* используются для раздела FAQ в виджете «FAQ»

:::



#### Пример микро-разметки**:**

```
<script type="application/ld+json">
{
"@context" : "https://schema.org/",
"@type" : "FAQPage",
"mainEntity" : [ {
"@type" : "Question",
"name" : "Как быстро я получу свой заказ?",
"acceptedAnswer" : {
"@type" : "Answer",
"text" : "Для уточнения сроков доставки, положите товар в корзину. В правой части корзины вы увидите варианты доставок и точную дату."
}
</script>
```



:::info 

Следующие *теги* используются на всех страницах web-to-print сервиса TCS

:::



-  **Тип ORGANIZATION**

   -  name (наименование компании)



-  **Тип POSTALADDRESS**

   -  streetAddress

   -  telephone

   -  email

#### Пример:

```
 <div itemscope itemtype="http://schema.org/Organization">
    <meta itemprop="name" content="ООО «Ваша Типография»"/>
    <div itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
       <meta itemprop="streetAddress" content="1205016, Россия, Москва, ул.Дзержинского, д.101, строение 4."/>
    </div>
    <meta itemprop="telephone" content="8-800-775-8-644"/>
    <meta itemprop="email" content="info@vashatipografiya.ru"/>
</div>
```