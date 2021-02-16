---
title: Каноническое свойство PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319273"
---
# <a name="pidlidtimezone-canonical-property"></a>Каноническое свойство PidLidTimeZone

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает сведения о часовом поясе повторяющегося собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |LID_TIME_ZONE  <br/> |
|Набор свойств:  <br/> |PSETID_Meeting  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x0000000C  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Собрания  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство считывается только в том случае, если свойство **dispidApptRecur** ([PidLidAppointmentRecur)](pidlidappointmentrecur-canonical-property.md)не за установлено, но если свойство **LID_IS_RECURRING** ([PidLidIsRecurring)](pidlidisrecurring-canonical-property.md)имеет true, а свойство **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) — FALSE. В нижней части WORD индекс указывается в таблице, которая содержит сведения о часовом поясе. Из верхней части WORD считыется только самый высокий бит. Если этот бит установлен, то часовой пояс, на который ссылается ссылка, не будет соблюдать летнее время (DST), в противном случае будут следовать даты DST, подробные [в [MS-OXOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

