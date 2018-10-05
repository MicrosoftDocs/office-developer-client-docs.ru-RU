---
title: Каноническое свойство PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385111"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a>Каноническое свойство PidTagReadReceiptRequested

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если отправитель сообщения запрашивает системы обмена сообщениями для создания чтения отчета, когда получатель сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_READ_RECEIPT_REQUESTED  <br/> |
|Идентификатор:  <br/> |0x0029  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно быть присвоено значение TRUE для проверки значения свойства **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) и **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)).
  
Если сообщение с набором **PR_READ_RECEIPT_REQUESTED** удаляется или истекает до системы обмена сообщениями можно создать отчет о чтения, nonread отчет создается. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
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

