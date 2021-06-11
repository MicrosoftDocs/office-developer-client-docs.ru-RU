---
title: Каноническое свойство PidLidDistributionListOneOffMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335051"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>Каноническое свойство PidLidDistributionListOneOffMembers

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает список разных entryIds, которые соответствуют членам личного списка рассылки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidDLOneOffMembers  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008054  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Эти разовый EntryIds инкапсулируют имена и адреса электронной почты личных участников списка рассылки.
  
Если клиент или сервер задают это свойство, оно должно синхронизироваться с свойством **dispidDLMembers** [(PidLidDistributionListMembers).](pidliddistributionlistmembers-canonical-property.md)Для каждой записи в свойстве **dispidDLOneOffMembers** должна быть запись в том же положении в свойстве **dispidDLMembers.** 
  
При настройке **dispidDLOneOffMembers** клиент или сервер должны убедиться, что его общий размер не превышает 15 000 bytes в размере.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

