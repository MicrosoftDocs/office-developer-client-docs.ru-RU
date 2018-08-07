---
title: Каноническое свойство PidTagMemberId
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
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811362"
---
# <a name="pidtagmemberid-canonical-property"></a>Каноническое свойство PidTagMemberId

  
  
**Относится к**: Outlook 
  
Содержит идентификатор элемента в таблице, имеющей описано права на почтового ящика или папки Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MEMBER_ID  <br/> |
|Идентификатор:  <br/> |0x6671  <br/> |
|Тип данных:  <br/> |PT_I8  <br/> |
|Область:  <br/> |Управление доступом  <br/> |
   
## <a name="remarks"></a>Замечания

Данное свойство возвращает уникальный идентификатор в таблицу. Идентификатор пользователя каталог связан с каждой идентификатор элемента и заданную с помощью этого свойства. Это свойство используется интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) получить идентификатор записи каталога элемента с помощью явных права на папку. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

