---
title: Каноническое свойство PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 760196668ffb3c486803f27b50ff809177e8e6f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588617"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Каноническое свойство PidTagTnefCorrelationKey

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение, соответствующее подключение к транспорта Neutral Encapsulation формата TNEF с сообщением.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Идентификатор:  <br/> |0x007F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется указывать, что дочерним объектам вложения TNEF данное свойство. Это свойство определяет, принадлежит ли файл входящих TNEF сообщение, которое он подключен к. Он используется в основном с поставщиками транспорта и шлюзов.
  
На исходящее сообщение поставщика транспорта должен compute двоичное значение, уникальным для этого сообщения или использовать существующее значение, которая должна удовлетворять требования уникальности, такие как идентификатор сообщения. Поставщика транспорта следует хранить это значение в это свойство и затем вызвать метод [ITnef::AddProps](itnef-addprops.md) для его инкапсуляции. Такое же значение также должны храниться в конверте транспорта на месте, определенные поставщиком, такие как заголовок сообщения. 
  
На входящих сообщений поставщика транспорта необходимо вызвать метод [ITnef::ExtractProps](itnef-extractprops.md) для decapsulate вложения TNEF и сравните это свойство со значением, хранящиеся в конверте транспорта. Если значения совпадают, TNEF обрабатывается обычным способом, то есть, следует использовать все свойства, извлеченные из вложения TNEF. Если значения не совпадают, все свойства из вложения TNEF можно пропустить. Если это свойство не задано, в файл формата TNEF должны считаться принадлежать на это сообщение и другие свойства, извлеченные из его следует использовать. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

