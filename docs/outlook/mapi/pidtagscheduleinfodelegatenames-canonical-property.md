---
title: Каноническое свойство PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314940"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a>Каноническое свойство PidTagScheduleInfoDelegateNames

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имена делегатов.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W  <br/> |
|Идентификатор:  <br/> |0x6844  <br/> |
|Тип данных:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

Каждая запись в этих свойствах должна содержать значение **свойства PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)адресной книги каждого делегата.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы подключения к почтовым ящикам и настройки их в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.
    
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

