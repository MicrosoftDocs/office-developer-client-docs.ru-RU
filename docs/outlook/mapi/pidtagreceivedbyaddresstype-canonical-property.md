---
title: Каноническое свойство PidTagReceivedByAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382668"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a>Каноническое свойство PidTagReceivedByAddressType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тип адреса электронной почты, таких как SMTP, для обмена сообщениями пользователя, который получает сообщение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W  <br/> |
|Идентификатор:  <br/> |0x0075  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями пользователя, который получает сообщение. Им должен иметь значение входящих поставщика транспорта.
  
Строка тип адреса может содержать только прописные буквы от A до Z и чисел нулевой до девяти. Эти свойства уточнения свойство **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)), указав тип адреса, например SMTP, таким образом, указывающее, как адрес должен быть создан.
  
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
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

