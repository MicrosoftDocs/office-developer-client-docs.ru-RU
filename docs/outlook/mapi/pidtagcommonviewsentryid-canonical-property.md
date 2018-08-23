---
title: Каноническое свойство PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7449e59227b147d34c2329175d0251dbb9c427b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581344"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Каноническое свойство PidTagCommonViewsEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи предварительно определенные общие папки представления. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x35E6  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Приложения Outlook  <br/> |
   
## <a name="remarks"></a>Замечания

Общие папки представление содержит с предопределенным набором описатели стандартного представления, а представление папки описатели, определенные пользователем, обмена мгновенными сообщениями. Эти папки, которые не отображаются в иерархии электронной почты — это сообщение (IPM), может содержать множество спецификаторы представления, каждая из которых хранятся в виде сообщения. Клиентское приложение можно выбрать объединение двух наборов указателей и сделать их оба доступными. 
  
Дополнительные сведения о представлениях содержатся [Представления папок](mapi-view-folders.md).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)
  
[Каноническое свойство PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

