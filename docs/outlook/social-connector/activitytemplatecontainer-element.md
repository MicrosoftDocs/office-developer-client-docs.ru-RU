---
title: элемент activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Элемент activityTemplateContainer — это шаблон, который позволяет форматировать элементы ленты действий и повторно использовать XML, который указывает макет.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413719"
---
# <a name="activitytemplatecontainer-element"></a>элемент activityTemplateContainer

Элемент **activityTemplateContainer** — это шаблон, который позволяет форматировать элементы ленты действий и повторно использовать XML, который указывает макет. Используйте ID **(applicationID** и **templateID),** чтобы соответствовать элементу feed **(activityDetails)** шаблону **(activityTemplateContainer).** Хранение данных макета в составе **элемента activityTemplate.** Чтобы ссылаться на данные, извлекаемые из отдельного элемента ленты действий, используйте переменные шаблона в качестве задатчиков для получения сведений, таких как люди, ссылки и текст. 
  
В следующей таблице описываются три элемента, необходимые **элементу activityTemplateContainer.** 
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**applicationID** <br/> |Один из двух уникальных ИД, используемых для совпадения элемента ленты с его шаблоном. Если у вас несколько приложений или других групп, это можно использовать в качестве организатора шаблонов первого уровня.  <br/> |
|**templateID** <br/> |Второй уникальный ID, который используется для совпадения элемента ленты с его шаблоном. Это можно использовать в качестве организатора шаблонов второго уровня.  <br/> |
|**activityTemplate** <br/> |Макет шаблона **(значок,** **заголовок** и элементы данных) и тип действия **(элемент** типа).   <br/> |
   
В следующей таблице описываются детские элементы **activityTemplate,** описывающие макет и тип шаблона.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**icon** <br/> |Маркер ссылки, который ссылается на URL-адрес значка для этого элемента ленты.  <br/> |
|**заголовок** <br/> |Необходимые сведения для элемента ленты.  <br/> |
|**type** <br/> |Тип действия, например обновление состояния, фотографии или документа.  <br/> |
|**data** <br/> |Любые дополнительные сведения для элемента ленты, такие как изображения, текст или ссылки.  <br/> |
   
Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)
  
## <a name="see-also"></a>См. также

- [Обзор XML для элемента ленты действий](overview-of-xml-for-an-activity-feed-item.md)  
- [элемент activityDetails](activitydetails-element.md)  
- [Переменные шаблона](template-variables.md)  
- [Рекомендации для правильного отображения действий](guidelines-for-properly-displaying-activities.md)  
- [XML для действий](xml-for-activities.md)  
- [Outlook Схема поставщика социальных соединителем XML](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

