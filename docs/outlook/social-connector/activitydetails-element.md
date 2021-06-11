---
title: элемент activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails сохраняет необработанные данные для одного элемента ленты действий. Каждый элемент ленты действий должен иметь свой элемент activityDetails. Данные в элементе activityDetails ссылаются в шаблонах действий с помощью элементов имен.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434874"
---
# <a name="activitydetails-element"></a>элемент activityDetails

Элемент **activityDetails сохраняет** необработанные данные для одного элемента ленты действий. Каждый элемент ленты действий должен иметь свой **элемент activityDetails.** Данные в **элементе activityDetails** ссылаются в шаблонах действий с помощью **элементов имен.** Каждый элемент данных в **элементе activityDetails должен** иметь **элемент name.** 
  
В следующей таблице описываются шесть элементов, необходимых **элементу activityDetails.** 
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**ownerID** <br/> |ID пользователя в социальной сети, сгенерившего этот элемент ленты действий.  <br/> |
|**objectID** <br/> |Уникальная строка для элемента ленты действий для обнаружения дублирующих элементов каналов.  <br/> |
|**applicationId** <br/> |Один из двух уникальных ИД, используемых для совпадения элемента ленты действий с его шаблоном. Если у вас несколько приложений или других групп, это можно использовать в качестве организатора шаблонов первого уровня.  <br/> |
|**templateId** <br/> |Второй уникальный ID, используемый для совпадения элемента ленты действий с его шаблоном. Это можно использовать в качестве организатора шаблонов второго уровня.  <br/> |
|**publishDate** <br/> |Дата и время публикации элемента ленты действий.  <br/> |
|**templateVariables** <br/> |Данные, которые будут использоваться в маркерах для шаблона элемента ленты действий.  <br/> |
   
Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)
  
## <a name="see-also"></a>См. также

- [Обзор XML для элемента ленты действий](overview-of-xml-for-an-activity-feed-item.md)  
- [элемент activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Переменные шаблона](template-variables.md) 
- [Рекомендации для правильного отображения действий](guidelines-for-properly-displaying-activities.md)  
- [XML для действий](xml-for-activities.md)  
- [Outlook Схема поставщика социальных соединителем XML](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

