---
title: Каноническое свойство PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389766"
---
# <a name="pidtagconversationkey-canonical-property"></a>Каноническое свойство PidTagConversationKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит беседы ключ, используемый в Microsoft Outlook только в том случае, если поиск **IPM. MessageManager** сообщения, такие как сообщение, содержащее истории загрузки для учетной записи Post Office Protocol (POP3). Это свойство является устаревшим в Microsoft Exchange Server. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Идентификатор:  <br/> |0x000B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

При доступе к сообщениям электронной почты как бесед и преобразование свойства сообщения в [Transport-Neutral Encapsulation формата TNEF ()](transport-neutral-encapsulation-format-tnef.md), не используйте это свойство; Используйте свойства каноническое [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Поддерево IPM](ipm-subtree.md)
  
[����������� ����� MAPI](mapi-special-folders.md)
  
[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

