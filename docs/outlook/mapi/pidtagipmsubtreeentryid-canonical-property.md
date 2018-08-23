---
title: Каноническое свойство PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ade74b13811445c39c73f778b6de49b67b59093b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587560"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>Каноническое свойство PidTagIpmSubtreeEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи корня поддерево папки электронной почты — это сообщение (IPM) в дереве папки хранилища сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IPM_SUBTREE_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x35E0  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство представляет корень иерархии IPM. IPM клиенты не должны отображаться какие-либо папки, которые не являются вложенные папки, представленного в этом свойстве.
  
## <a name="related-resources"></a>Связанные ресурсы

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

