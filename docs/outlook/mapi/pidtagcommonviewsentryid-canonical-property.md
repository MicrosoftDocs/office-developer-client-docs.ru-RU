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
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437345"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Каноническое свойство PidTagCommonViewsEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи предопределяемой общей папки представления. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x35E6  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Приложение Outlook  <br/> |
   
## <a name="remarks"></a>Примечания

Общая папка представления содержит предварительно определенный набор стандартных определителей представления, а папка представления содержит определители, определенные пользователем системы обмена сообщениями. В этих папках, которые не видны в иерархии межличностных сообщений (IPM), может храниться множество о указаний представления, каждая из которых хранится в качестве сообщения. Клиентские приложения могут объединить два набора о указаний и сделать их доступными. 
  
Дополнительные сведения о представлениях см. в [просмотре папок.](mapi-view-folders.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)
  
[Каноническое свойство PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

