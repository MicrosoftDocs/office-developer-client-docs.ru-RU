---
title: Каноническое свойство PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811574"
---
# <a name="pidtagprofilename-canonical-property"></a>Каноническое свойство PidTagProfileName

  
  
**Относится к**: Outlook 
  
Содержит имя профиля.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3D12  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Настройки профилей MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства вычисляются поставщиками услуг. Реализация поставщика функции **на неизвестную запись сервиса** можно использовать эти свойства для обнаружения имя профиля. 
  
Клиентские приложения могут использовать эти свойства как удобной альтернативы для получения имени профиля, проверив свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в строке состояния таблицы подсистемы MAPI.
  
Эти свойства могут быть уникальным во времени, например где профиль удаляется и более поздних версий заново с таким же именем. MAPI предоставляющей полностью уникальные свойства **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) в разделе жестко заданного профиля **MUID_PROFILE_INSTANCE.**
  
## <a name="related-resources"></a>Связанные ресурсы

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

