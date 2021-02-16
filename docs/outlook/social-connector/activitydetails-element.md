---
title: Элемент activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails сохраняет необработанные данные для одного элемента веб-канала активности. Каждый элемент веб-канала активности должен иметь собственный элемент activityDetails. На данные в элементе activityDetails ссылается шаблоны действий с помощью элементов name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434874"
---
# <a name="activitydetails-element"></a>Элемент activityDetails

Элемент **activityDetails сохраняет** необработанные данные для одного элемента веб-канала активности. Каждый элемент веб-канала активности должен иметь собственный **элемент activityDetails.** На данные в **элементе activityDetails** ссылается шаблоны действий с помощью **элементов** name. Каждый элемент данных в **элементе activityDetails** должен иметь **элемент name.** 
  
В следующей таблице описываются шесть элементов, необходимых **элементу activityDetails.** 
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**ownerID** <br/> |ИД пользователя в социальной сети, который вызвал этот элемент веб-канала активности.  <br/> |
|**objectID** <br/> |Уникальная строка для элемента веб-канала активности для обнаружения дублирующихся элементов веб-канала.  <br/> |
|**applicationId** <br/> |Один из двух уникальных ИД, используемых для совпадения элемента веб-канала активности с его шаблоном. Если у вас несколько приложений или групп, его можно использовать в качестве организатора шаблонов первого уровня.  <br/> |
|**templateId** <br/> |Второй уникальный ИД, используемый для совпадения элемента веб-канала активности с его шаблоном. Его можно использовать в качестве организатора шаблонов второго уровня.  <br/> |
|**publishDate** <br/> |Дата и время публикации элемента веб-канала активности.  <br/> |
|**templateVariables** <br/> |Данные, используемые в маркерах для шаблона элемента веб-канала активности.  <br/> |
   
Пример XML-канала активности см. в [XML-примере веб-канала активности](activity-feed-xml-example.md)
  
## <a name="see-also"></a>См. также

- [Обзор XML для элемента веб-канала активности](overview-of-xml-for-an-activity-feed-item.md)  
- [Элемент activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Переменные шаблона](template-variables.md) 
- [Руководство по правильному отобралку действий](guidelines-for-properly-displaying-activities.md)  
- [XML для действий](xml-for-activities.md)  
- [XML-схема поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с помощью схемы OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

