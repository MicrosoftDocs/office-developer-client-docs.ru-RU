---
title: Элемент activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Элемент activityDetails хранит необработанные данные для одного элемента веб-канала активности. Каждый элемент веб-канала активности должен иметь собственный элемент activityDetails. К данным в элементе activityDetails ссылаются шаблоны действий с помощью элементов name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434874"
---
# <a name="activitydetails-element"></a>Элемент activityDetails

Элемент **activityDetails** хранит необработанные данные для одного элемента веб-канала активности. Каждый элемент веб-канала активности должен иметь собственный элемент **activityDetails** . К данным в элементе **activityDetails** ссылаются шаблоны действий с помощью элементов **Name** . У каждого фрагмента данных в элементе **activityDetails** должен быть элемент **Name** . 
  
В следующей таблице описываются шесть элементов, необходимых для элемента **activityDetails** . 
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**овнерид** <br/> |Идентификатор пользователя в социальной сети, создавшего этот элемент веб-канала активности.  <br/> |
|**ИД** <br/> |Уникальная строка для элемента веб-канала активности для обнаружения повторяющихся элементов веб-канала.  <br/> |
|**applicationId** <br/> |Один из двух уникальных идентификаторов, которые используются для сравнения элемента канала активности с его шаблоном. При наличии нескольких приложений или других групп их можно использовать в качестве организатора шаблонов первого уровня.  <br/> |
|**templateId** <br/> |Второй уникальный идентификатор, который используется для сравнения элемента канала активности с его шаблоном. Его можно использовать в качестве организатора шаблонов второго уровня.  <br/> |
|**публишдате** <br/> |Дата и время публикации элемента веб-канала активности.  <br/> |
|**темплатевариаблес** <br/> |Данные, которые будут использоваться в маркерах для шаблона элемента веб-канала активности.  <br/> |
   
Пример XML-кода канала активности представлен в статье [Пример XML-канала активности](activity-feed-xml-example.md)
  
## <a name="see-also"></a>См. также

- [Обзор XML-файла для элемента веб-канала активности](overview-of-xml-for-an-activity-feed-item.md)  
- [Элемент activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Переменные шаблона](template-variables.md) 
- [Рекомендации по правильному отображению действий](guidelines-for-properly-displaying-activities.md)  
- [XML для действий](xml-for-activities.md)  
- [Схема XML поставщика социальных соединителей Outlook](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с помощью XML-схемы OSC](developing-a-provider-with-the-osc-xml-schema.md)

