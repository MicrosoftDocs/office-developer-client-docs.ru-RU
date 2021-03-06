---
title: Переменные шаблонов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Экземпляры переменных шаблонов (представленные элементом templateVariable) указывают данные элемента ленты действий в шаблоне действий.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404374"
---
# <a name="template-variables"></a>Переменные шаблонов

Экземпляры переменных шаблонов (представленные элементом **templateVariable)** указывают данные элемента ленты действий в шаблоне действий. 
  
Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)

В следующей таблице показаны типы поддерживаемых переменных шаблонов, каждая из которых представлена соответствующим значением XML-индексации.
  
|**Тип переменной шаблона**|**Описание**|
|:-----|:-----|
|**entityVariable** <br/> |Человек, группа или вещь.  <br/> |
|**linkVariable** <br/> |Ссылка.  <br/> |
|**listVariable** <br/> |Группа объектов.  <br/> |
|**pictureVariable** <br/> |Изображение.  <br/> |
|**publisherVariable** <br/> |Издатель элемента ленты действий.  <br/> |
|**textVariable** <br/> |Блок текста.  <br/> |
   
Каждый тип переменной шаблона имеет необходимые элементы для указания данных об этой переменной. Переменные шаблона указаны следующим образом:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Переменная шаблона списка

Можно указать переменные шаблона, содержащиеся в списке (делимитированные элементами **listVariable** и **listItems)** следующим образом: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Переменная шаблона **типа listVariable** — это контейнер для объектов. Он может содержать запятые элементы (типа **linkVariable** или **textVariable)** или изображения (типа **pictureVariable).** Списки могут содержать до пяти элементов ссылок, пять текстовых элементов или пять изображений. 
  
В Outlook social Connector (OSC) локализованы элементы списка ссылок или текстов в соответствии с Windows локальной системой.
  
Чтобы правильно разобрать и отобразить изображения в элементе ленты действий, необходимо включить изображения в список. Размер всех изображений составляет 52 пикселя. Ширина изображения не resized.
  
## <a name="template-variable-elements"></a>Элементы переменной шаблона

В этом разделе охватываются необходимые и необязательные элементы, поддерживаемые для каждого типа переменной шаблона.
  
### <a name="entityvariable"></a>entityVariable

|**Элемент**|**Описание**|
|:-----|:-----|
|**name** <br/> |Имя переменной. Обязательный.  <br/> |
|**id** <br/> |Уникальный ID пользователя. Обязательный.  <br/> |
|**nameHint** <br/> |Имя, отображаемая в элементе ленты. Необязательный параметр.  <br/> |
|**profileUrl** <br/> |URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе ленты, если его имя присутствует. Необязательный параметр.  <br/> |
|**emailAddress** <br/> |Адрес электронной почты, используемый для обновления контактных данных этого лица в Outlook. Необязательный параметр.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Элемент**|**Описание**|
|:-----|:-----|
|**name** <br/> |Имя переменной. Обязательный.  <br/> |
|**value** <br/> |URL-адрес этой ссылки. Обязательный.  <br/> |
|**text** <br/> |Текст ссылки, отображаемой вместо самого URL-адреса. Необязательный параметр.  <br/> |
   
### <a name="listvariable"></a>listVariable

|**Элемент**|**Описание**|
|:-----|:-----|
|**name** <br/> |Имя переменной. Обязательный.  <br/> |
|**listItems** <br/> |Контейнер для элементов в списке. Обязательный.  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**Элемент**|**Описание**|
|:-----|:-----|
|**name** <br/> |Имя переменной. Обязательный.  <br/> |
|**value** <br/> |URL-адрес для изображения. Обязательный.  <br/> |
|**altText** <br/> |Альтернативный текст, отображаемый для доступности и когда пользователь перемещает указатель мыши по изображению. Необязательный параметр.  <br/> |
|**href** <br/> |Гиперссылка, используемая при щелчке изображения пользователем, если желаемая цель не является URL-адресом изображения, указанным элементом **значения.** Необязательный параметр.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Элемент**|**Описание**|
|:-----|:-----|
|**name** <br/> |Имя переменной. Обязательный.  <br/> |
|**id** <br/> |Уникальный ID пользователя. Обязательный.  <br/> |
|**nameHint** <br/> |Имя, отображаемая в элементе ленты. Необязательный параметр.  <br/> |
|**profileUrl** <br/> |URL-адрес профиля пользователя, который будет использоваться в качестве гиперссылки для имени пользователя в элементе ленты, если его имя присутствует. Необязательный параметр.  <br/> |
|**emailAddress** <br/> |Адрес электронной почты, используемый для обновления контактных данных этого лица в Outlook. Необязательный параметр.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Элемент**|**Описание**|
|:-----|:-----|
|**name** <br/> |Имя переменной. Обязательный.  <br/> |
|**value** <br/> |Текст для отображения. Необязательный параметр.  <br/> |
   
## <a name="see-also"></a>См. также

- [Обзор XML для элемента ленты действий](overview-of-xml-for-an-activity-feed-item.md)  
- [элемент activityDetails](activitydetails-element.md)  
- [элемент activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Рекомендации для правильного отображения действий](guidelines-for-properly-displaying-activities.md)  
- [XML для действий](xml-for-activities.md)  
- [Outlook Схема поставщика социальных соединителем XML](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

