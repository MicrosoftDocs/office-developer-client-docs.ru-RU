---
title: activityDetails элемент
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails хранит необработанные данные для отдельного веб-канала элемента действия. Каждый веб-канал элементов активности должен иметь собственный элемент activityDetails. Данные в элементе activityDetails используется в шаблоны действий с помощью имени элементов.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812710"
---
# <a name="activitydetails-element"></a>activityDetails элемент

Элемент **activityDetails** хранит необработанные данные для отдельного веб-канала элемента действия. Каждый веб-канал элементов активности должен иметь собственный элемент **activityDetails** . Данные в элементе **activityDetails** используется в шаблоны действий с помощью **имени** элементов. Каждый элемент данных в элементе **activityDetails** должен иметь **имя** элемента. 
  
В следующей таблице описаны шесть элементов, которого требует элемент **activityDetails** . 
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**ownerID** <br/> |Идентификатор пользователя, социальные сети, созданного действия веб-канала элемента.  <br/> |
|**objectID** <br/> |Уникальная строка для действия веб-канала элемента для обнаружения повторяющихся элементов веб-канала.  <br/> |
|**applicationId** <br/> |Один из двух уникальных идентификаторов, которые используются в соответствии с действия веб-канала элемента с шаблоном. При наличии нескольких приложений или других групп, это можно использовать в качестве шаблона первого уровня Организатор.  <br/> |
|**templateId** <br/> |Второй уникальный идентификатор, используемый для сопоставления для действия веб-канала элемента с шаблоном. Это можно использовать в качестве организатора шаблона второго уровня.  <br/> |
|**publishDate** <br/> |Дата и время элемента веб-канала активности была опубликована.  <br/> |
|**templateVariables** <br/> |Данные для использования в маркеры для шаблона элемента веб-канала активности.  <br/> |
   
Пример активности веб-канала XML, содержатся в [Примере XML веб-канала активности](activity-feed-xml-example.md)
  
## <a name="see-also"></a>См. также

- [Общие сведения о XML-код для действия элемента веб-канала](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer элемент](activitytemplatecontainer-element.md)  
- [Переменные шаблона](template-variables.md) 
- [Рекомендации для правильного отображения действий](guidelines-for-properly-displaying-activities.md)  
- [XML-код для действия](xml-for-activities.md)  
- [Схема XML поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с использованием схемы XML для OSC](developing-a-provider-with-the-osc-xml-schema.md)

