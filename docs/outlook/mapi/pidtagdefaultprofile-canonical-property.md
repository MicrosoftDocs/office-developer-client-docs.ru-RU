---
title: Каноническое свойство PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811026"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Каноническое свойство PidTagDefaultProfile

  
  
**Относится к**: Outlook 
  
Содержит значение TRUE, если профиль пользователя обмена сообщениями является профилем по умолчанию MAPI.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|Идентификатор:  <br/> |0x3D04  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не отображается как свойство какого-либо объекта, но только в виде столбцов в таблице профилей. Клиентское приложение можно использовать метод [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) для обозначения профиля по умолчанию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
