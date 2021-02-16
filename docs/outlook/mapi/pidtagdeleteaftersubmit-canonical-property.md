---
title: Каноническое свойство PidTagDeleteAfterSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359916"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a>Каноническое свойство PidTagDeleteAfterSubmit

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если клиентского приложения хочет MAPI удалить связанное сообщение после отправки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELETE_AFTER_SUBMIT  <br/> |
|Идентификатор:  <br/> |0x0E01  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |MAPI, не передаваемый  <br/> |
   
## <a name="remarks"></a>Примечания

Клиентские приложения используют это свойство со свойством **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)для управления тем, что происходит с сообщением после его отправки. Следует установить один или несколько из них, но не оба. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для основных объектов хранения сообщений.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

