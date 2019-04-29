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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если пользователю обмена сообщениями разрешено отправлять и получать сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_МАИЛ_ПЕРМИССИОН  <br/> |
|Идентификатор:  <br/> |0x3A0E  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство не задано, MAPI рассматривает его как имеющий значение TRUE. 
  
Установите для этого свойства значение FALSE в корпоративном каталоге, в котором для некоторых записей не включена поддержка электронной почты. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

