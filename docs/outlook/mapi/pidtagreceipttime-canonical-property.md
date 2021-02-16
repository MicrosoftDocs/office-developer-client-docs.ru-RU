---
title: Каноническое свойство PidTagReceiptTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiptTime
api_type:
- COM
ms.assetid: 9c6cd2f4-e769-4786-b9cc-c02641fecc4f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd332943d8264ff909c1ec36f6b7c939d597acfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432186"
---
# <a name="pidtagreceipttime-canonical-property"></a>Каноническое свойство PidTagReceiptTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит дату и время, когда создается отчет о доставке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECEIPT_TIME  <br/> |
|Идентификатор:  <br/> |0x002A  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть установлено поставщиком store сообщений, который получает исходное сообщение и создает отчет. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

