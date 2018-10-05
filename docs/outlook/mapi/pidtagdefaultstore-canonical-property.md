---
title: Каноническое свойство PidTagDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385167"
---
# <a name="pidtagdefaultstore-canonical-property"></a>Каноническое свойство PidTagDefaultStore

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если хранилища сообщений — это хранилище сообщений по умолчанию в таблице хранилища сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFAULT_STORE  <br/> |
|Идентификатор:  <br/> |0x3400  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Хранение сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство в виде столбцов в таблице хранилища сообщений. Значение основано на **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
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

