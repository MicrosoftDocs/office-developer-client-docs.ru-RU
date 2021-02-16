---
title: Каноническое свойство PidTagOwnerAppointmentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ad68a8ba527879871e79dd85e79d577291d32a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335443"
---
# <a name="pidtagownerappointmentid-canonical-property"></a>Каноническое свойство PidTagOwnerAppointmentId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор встречи в расписании владельца.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_OWNER_APPT_ID  <br/> |
|Идентификатор:  <br/> |0x0062  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Appointment  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется в запросах на собрание. Он не представляет идентификатор записи, а длинное integer, которое однозначно определяет встречу в расписании отправителем.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagOriginalAuthorSearchKey](pidtagoriginalauthorsearchkey-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

