---
title: Каноническое свойство PidTagScheduleInfoDelegatorWantsCopy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegatorWantsCopy
api_type:
- COM
ms.assetid: 48e48e3a-1186-46c4-8ff9-34e03905fb93
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c52a1c055792f17477ff5540c4138160544e3b18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321310"
---
# <a name="pidtagscheduleinfodelegatorwantscopy-canonical-property"></a>Каноническое свойство PidTagScheduleInfoDelegatorWantsCopy

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если делегатор хочет получать копии объектов, связанных с собраниями, которые отправляются делегату.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_BOSS_WANTS_COPY  <br/> |
|Идентификатор:  <br/> |0x6842  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть заданной в информационном объекте делегирования.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы подключения к почтовым ящикам и настройки их в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Публикует доступность пользователя или ресурса.
    
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

