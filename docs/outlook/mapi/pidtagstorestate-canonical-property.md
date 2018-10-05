---
title: Каноническое свойство PidTagStoreState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399013"
---
# <a name="pidtagstorestate-canonical-property"></a>Каноническое свойство PidTagStoreState

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит флаг, который описывает состояние хранилища сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STORE_STATE  <br/> |
|Идентификатор:  <br/> |0x340E  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Хранение сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является динамическим и может изменяться в зависимости от действий пользователя, в отличие от свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
Может быть установлено следующее значение:
  
STORE_HAS_SEARCHES 
  
> Пользователь мог создать один или несколько активных поисков в хранилище.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для базовых объектов хранилища сообщений.
    
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

