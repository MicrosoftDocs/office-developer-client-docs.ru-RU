---
title: Каноническое свойство PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395128"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Каноническое свойство PidTagRecipientReassignmentProhibited

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Запрещение ли добавление дополнительных получателей при пересылке сообщения, для сообщения электронной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Идентификатор:  <br/> |0x002B  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство устанавливается на основе значение **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) сообщения электронной почты. Если **PR_SENSITIVITY** задано значение «0x00000000» (обычный) или «0x00000003» (confidential), это свойство необходимо установить для «0x00» или отсутствует означает, что добавление дополнительных или других получателей на сообщение электронной почты, разрешено. Если сообщение электронной почты объекта **PR_SENSITIVITY** задано значение «0x00000001» (личные) или «0x00000002» (личные), это свойство должно иметь значение «0x01» для предотвращения добавления дополнительных или других получателей в этом электронной почты через переадресации. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые в сообщениях электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

