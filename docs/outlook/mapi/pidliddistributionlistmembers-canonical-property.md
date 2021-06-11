---
title: Каноническое свойство PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335072"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Каноническое свойство PidLidDistributionListMembers

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает список entryIds объектов, соответствующих членам личного списка рассылки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidDLMembers  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008055  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Членами личного списка рассылки могут быть другие личные списки рассылки, электронные адреса, содержащиеся в контакте, пользователи глобального списка адресов или списки рассылки, а также разовая электронная почта. Формат каждого EntryId должен быть либо разовый EntryId, как указано [в [MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) либо завернутый EntryId. 
  
При настройке этого свойства клиент или сервер должны убедиться, что его общий размер не превышает 15 000 bytes.
  
В этом свойстве указан список разных entryIds, которые соответствуют членам личного списка рассылки. Эти разовый EntryIds инкапсулируют имена и адреса электронной почты личных участников списка рассылки.
  
Если клиент или сервер задают это свойство, оно должно быть синхронизировано с этим свойством **dispidDDLMembers** для каждой записи в **dispidDLOneOffMembers** [(свойство PidLidDistributionListOneOffMembers),](pidliddistributionlistoneoffmembers-canonical-property.md)должна быть запись в том же положении в **dispidDLOneOffMembers**.
  
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

