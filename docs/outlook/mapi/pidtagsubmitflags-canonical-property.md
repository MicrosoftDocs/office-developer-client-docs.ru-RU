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
ms.openlocfilehash: fb048d622aaf3cfa97f380e21324749d7421603e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563690"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Каноническое свойство PidTagSubmitFlags

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску флагов, указывающее, подробные сведения о отправки сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Идентификатор:  <br/> |0x0E14  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Один или несколько из следующих флагов можно задать для битовой маски **PR_SUBMIT_FLAGS** : 
  
SUBMITFLAG_LOCKED 
  
> Диспетчер очереди MAPI в настоящее время имеет сообщение блокируется. 
    
SUBMITFLAG_PREPROCESS 
  
> Сообщение должно предварительной обработки. Когда выполняется диспетчер очереди MAPI предварительной обработки это сообщение, его необходимо вызвать метод [IMessage::SubmitMessage](imessage-submitmessage.md) . Поставщик хранения сообщений обнаруживает, что диспетчер очереди, а не клиентского приложения называется **SubmitMessage**, сбрасывает и по-прежнему производится передача сообщений.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

