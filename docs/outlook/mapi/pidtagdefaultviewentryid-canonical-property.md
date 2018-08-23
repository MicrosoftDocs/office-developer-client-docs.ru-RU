---
title: Каноническое свойство PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2c941ea43a19b51e46c00b37aa89f504c55f180a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587210"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Каноническое свойство PidTagDefaultViewEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи представления по умолчанию папки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x3616  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство соответствует записи идентификатор представления папок, который следует задать как начальное представление. Не требуется набора свойств, если представление «Обычный» для использования в качестве начальное представление.
  
Клиентское приложение может получить это свойство во время, когда она открывается папку и реализовать существенно повысить производительность. Это свойство можно использовать для быстрого получить представление по умолчанию, вместо открытия связанного содержимого таблицы и отправка ограничение.
  
Реализация поставщика службы метода [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) можно скопировать это свойство, при копировании папки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

