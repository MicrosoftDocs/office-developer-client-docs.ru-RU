---
title: Каноническое свойство PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427313"
---
# <a name="pidtagviewsentryid-canonical-property"></a>Каноническое свойство PidTagViewsEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор входа в папку Представления, определяемую пользователем.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_VIEWS_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x35E5  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Хранилище сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Общая папка представления содержит заданный набор стандартных оговарителей представления, а папка представлений содержит оговарители, определенные пользователем обмена сообщениями. Эти папки, которые не видны в иерархии межличностных сообщений (IPM), могут вметь множество задающих представлений, каждая из которых хранится в качестве сообщения. Клиентская заявка может объединить два набора оговарителей и сделать их доступными.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

