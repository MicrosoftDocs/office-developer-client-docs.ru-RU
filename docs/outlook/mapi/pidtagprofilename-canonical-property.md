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
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435651"
---
# <a name="pidtagprofilename-canonical-property"></a>Каноническое свойство PidTagProfileName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя профиля.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3D12  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Конфигурация профиля MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства вычисляются поставщиками услуг. Реализация функции **ServiceEntry** поставщика может использовать эти свойства для обнаружения имени профиля. 
  
Клиентские приложения могут использовать эти свойства в качестве удобной альтернативы получению имени **профиля,** изучив свойство [PR_DISPLAY_NAME (PidTagDisplayName)](pidtagdisplayname-canonical-property.md)в строке таблицы состояния MAPI.
  
Эти свойства не могут быть уникальными во времени, например, когда профиль удаляется и затем воссоздается с тем же именем. MAPI обставлено уникальным свойством **PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)в жестко закодированном разделе профилей **MUID_PROFILE_INSTANCE.**
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

