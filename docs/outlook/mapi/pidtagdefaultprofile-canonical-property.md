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
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428776"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>Каноническое свойство PidTagDefaultProfile

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если профиль пользователя обмена сообщениями является профилем по умолчанию MAPI.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ДЕФАУЛТ_ПРОФИЛЕ  <br/> |
|Идентификатор:  <br/> |0x3D04  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не отображается как свойство какого бы то ни было объекта, но только как столбец в таблице профиля. Клиентское приложение может использовать метод [ипрофадмин:: SetDefaultProfile](iprofadmin-setdefaultprofile.md) , чтобы назначить профиль по умолчанию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

