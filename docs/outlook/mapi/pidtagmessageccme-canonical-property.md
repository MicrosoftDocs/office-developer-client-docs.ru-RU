---
title: Каноническое свойство PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 82d043adfe6e480b4d490f44ad89d73535c80c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569780"
---
# <a name="pidtagmessageccme-canonical-property"></a>Каноническое свойство PidTagMessageCcMe

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если этого обмена сообщениями пользователя специально с именем как получателей скрытой копии (CC) сообщения и не является частью списка рассылки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Идентификатор:  <br/> |0x0058  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство обеспечивает удобный способ для определения, является ли имя пользователя отображается явным образом из списка получателей скрытой копии без проверки всех записей в списке. 
  
Это свойство также используется для автоматической обработки сообщений, полученных во время поступления. В параметр поставщика транспорта это свойство содержит значение FALSE или не задано, если обмена сообщениями пользователя отсутствует в списке непосредственно в таблице получателей. 
  
Доставка сообщений, связанные с обозначение скрытой копии или раскрытие списков рассылки не вызывает это свойство должно быть задано. Получатель должно быть задано явным образом. 
  
Неотправленные сообщения, как правило, не задавайте это свойство, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) или **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). Если они имеются в сообщения, пользователь может получить доступ в хранилищах открытого сообщения, в частном другим пользователям хранилищ в файлы на диске, или встроенный других полученные сообщения, они как правило, содержат значения, к которым они были определенного последнего поставщика транспорта доставить сообщение. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

