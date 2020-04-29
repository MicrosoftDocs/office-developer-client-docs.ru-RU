---
title: Каноническое свойство PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339356"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Каноническое свойство PidTagSubmitFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску флагов, указывающих сведения об отправке сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Идентификатор:  <br/> |0x0E14  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Несъемный MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Для битовой маски **PR_SUBMIT_FLAGS** можно задать один или несколько следующих флагов: 
  
SUBMITFLAG_LOCKED 
  
> В настоящий момент сообщение заблокировано диспетчером очереди MAPI. 
    
SUBMITFLAG_PREPROCESS 
  
> Сообщение нуждается в предварительной обработке. Когда диспетчер очереди MAPI закончит предварительную обработку этого сообщения, он должен вызвать метод [iMessage:: субмитмессаже](imessage-submitmessage.md) . Поставщик хранилища сообщений распознает, что диспетчер очереди, а не клиентское приложение называется **субмитмессаже**, очищает флаг и продолжает отправку сообщения.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

