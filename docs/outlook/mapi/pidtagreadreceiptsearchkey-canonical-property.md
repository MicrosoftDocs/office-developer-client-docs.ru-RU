---
title: Каноническое свойство PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7016b1a7039d5df8d4e9fdedea580526eebe04bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585943"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a>Каноническое свойство PidTagReadReceiptSearchKey

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для обмена сообщениями пользователя, к которому система обмена сообщениями направляет просмотра отчетов для сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_READ_RECEIPT_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x0053  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство игнорируется, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) не установлен в значение TRUE.
  
Если клиентское приложение может принимать чтение отчетов, его можно оставить это свойство неопределенные или задайте для него значение ключа поиска, содержащихся в свойстве **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) во время отправки сообщения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые в сообщениях электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidef.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

