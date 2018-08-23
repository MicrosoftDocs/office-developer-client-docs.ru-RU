---
title: Каноническое свойство PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571194"
---
# <a name="pidtagmailpermission-canonical-property"></a>Каноническое свойство PidTagMailPermission

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если пользователь обмена сообщениями может отправлять и получать сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MAIL_PERMISSION  <br/> |
|Идентификатор:  <br/> |0x3A0E  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Замечания

Если это свойство не задано, MAPI обрабатывает ее как имеющий значение TRUE. 
  
Этому свойству присвоено значение FALSE в каталоге организации которых некоторые записи не включенной поддержкой электронной почты. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

