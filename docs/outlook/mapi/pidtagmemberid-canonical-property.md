---
title: Каноническое свойство PidTagMemberid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342639"
---
# <a name="pidtagmemberid-canonical-property"></a>Каноническое свойство PidTagMemberid

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор члена таблицы, который имеет описанные права на Microsoft Exchange Server папке или почтовом ящике.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MEMBER_ID  <br/> |
|Идентификатор:  <br/> |0x6671  <br/> |
|Тип данных:  <br/> |PT_I8  <br/> |
|Область:  <br/> |Управление доступом  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство возвращает идентификатор, уникальный для таблицы. Идентификатор пользователя каталога связан с каждым идентификатором участника и дается этим свойством. Это свойство используется [интерфейсом IExchangeModifyTable](iexchangemodifytableiunknown.md) для получения идентификатора записи каталога участника с явными правами на папку. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Обрабатывает ирисовку списков разрешений папок, хранимых на сервере.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

