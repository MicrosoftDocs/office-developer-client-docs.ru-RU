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
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430177"
---
# <a name="pidtagmailpermission-canonical-property"></a>Каноническое свойство PidTagMailPermission

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если пользователю обмена сообщениями разрешено отправлять и получать сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MAIL_PERMISSION  <br/> |
|Идентификатор:  <br/> |0x3A0E  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Адрес  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство не установлено, MAPI рассматривает его как значение TRUE. 
  
Установите это свойство false в корпоративном каталоге, где некоторые записи не включены по электронной почте. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

