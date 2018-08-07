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
ms.openlocfilehash: ae6202a1fdf7ec43bf2269236aa8120aa67e3c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810257"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>Каноническое свойство PidLidDistributionListOneOffMembers

  
  
**Относится к**: Outlook 
  
Задает список единичных записей, соответствующих членов списка рассылки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidDLOneOffMembers  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008054  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Эти единичных записей инкапсулируют отображаемые имена и адреса электронной почты из личного списка рассылки.
  
Если этому свойству присвоено клиент или сервер, должны быть синхронизированы с свойство **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)): для каждой записи в свойстве **dispidDLOneOffMembers** должно быть запись в том же Поместите в свойстве **dispidDLMembers** . 
  
При установке **dispidDLOneOffMembers**, клиент или сервер необходимо убедиться, что его общий размер является размером менее 15 000 байт.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

