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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356471"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a>Каноническое свойство PidTagReadReceiptRequested

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если отправитель сообщения хочет, чтобы система обмена сообщениями генерирула отчет о считывке, когда получатель читал сообщение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_READ_RECEIPT_REQUESTED  <br/> |
|Идентификатор:  <br/> |0x0029  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть задано true для проверки значений в **свойствах PR_READ_RECEIPT_ENTRYID** [(PidTagReadReceiptEntryId)](pidtagreadreceiptentryid-canonical-property.md)и **PR_READ_RECEIPT_SEARCH_KEY** [(PidTagReadReceiptSearchKey).](pidtagreadreceiptsearchkey-canonical-property.md)
  
Если сообщение с **PR_READ_RECEIPT_REQUESTED** или истекает до того, как система обмена сообщениями сможет создать отчет о прочтение, создается непрочитанные отчеты. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

