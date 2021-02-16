---
title: Элемент activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Элемент activityTemplateContainer — это шаблон, который позволяет форматировать элементы веб-канала активности и повторно использовать XML,который указывает макет.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413719"
---
# <a name="activitytemplatecontainer-element"></a>Элемент activityTemplateContainer

Элемент **activityTemplateContainer** — это шаблон, который позволяет форматировать элементы веб-канала активности и повторно использовать XML,который указывает макет. Используйте IDs **(applicationID** и **templateID)** для совпадения элемента веб-канала (**activityDetails**) с шаблоном (**activityTemplateContainer).** Храните данные макета как часть **элемента activityTemplate.** Для ссылки на данные, полученные из отдельного элемента веб-канала активности, используйте переменные шаблона в качестве замещего элемента для таких сведений, как люди, ссылки и текст. 
  
В следующей таблице описываются три элемента, необходимые элементу **activityTemplateContainer.** 
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**applicationID** <br/> |Один из двух уникальных ИД, используемых для совпадения элемента веб-канала с его шаблоном. Если у вас несколько приложений или групп, его можно использовать в качестве организатора шаблона первого уровня.  <br/> |
|**templateID** <br/> |Второй уникальный ИД, используемый для совпадения элемента веб-канала с его шаблоном. Его можно использовать в качестве организатора шаблонов второго уровня.  <br/> |
|**activityTemplate** <br/> |Макет шаблона **(значок,** **заголовок** и элементы данных) и тип действия **(элемент type).**   <br/> |
   
В следующей таблице описываются элементы **activityTemplate,** которые описывают макет и тип шаблона.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**icon** <br/> |Маркер ссылки, который ссылается на URL-адрес значка для этого элемента веб-канала.  <br/> |
|**заголовок** <br/> |Необходимые сведения для элемента веб-канала.  <br/> |
|**тип** <br/> |Тип действия, например обновление состояния, фотографии или документа.  <br/> |
|**data** <br/> |Любые дополнительные сведения об элементе веб-канала, такие как изображения, текст или ссылки.  <br/> |
   
Пример XML-канала активности см. в [XML-примере веб-канала активности](activity-feed-xml-example.md)
  
## <a name="see-also"></a>См. также

- [Обзор XML для элемента веб-канала активности](overview-of-xml-for-an-activity-feed-item.md)  
- [Элемент activityDetails](activitydetails-element.md)  
- [Переменные шаблона](template-variables.md)  
- [Руководство по правильному отобралку действий](guidelines-for-properly-displaying-activities.md)  
- [XML для действий](xml-for-activities.md)  
- [XML-схема поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с помощью схемы OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

