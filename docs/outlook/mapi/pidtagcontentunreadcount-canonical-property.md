---
title: Каноническое свойство PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331873"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Каноническое свойство PidTagContentUnreadCount

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит количество непрочитанные сообщения в папке, как вычислено в хранилище сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Идентификатор:  <br/> |0x3603  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство, вычисленное в хранилище сообщений, используется для двух различных, хотя и связанных, целей. На объекте папки MAPI содержится количество сообщений в папке. В строке заголовка в классизированных таблицах MAPI содержится количество непрочитанные не связанные сообщения в категории, соответствующей этой строке заголовка.
  
Это свойство содержит количество сообщений в таблице содержимого папки, для которых флаг MSGFLAG_READ не установлен в **свойстве PR_MESSAGE_FLAGS** [(PidTagMessageFlags).](pidtagmessageflags-canonical-property.md) Свойство **PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)содержит общее количество сообщений для папки. Клиенты **PR_CONTENT_COUNT** и это свойство только для чтения. 
  
Некоторые клиентские приложения отображают строку заголовка категории по-разному в зависимости от значения этого свойства. Например, клиент может отображать категорию, которая включает непрочитанные сообщения жирным шрифтом. Это свойство не может использоваться в качестве категории, и попытка сделать это приводит к возвращению MAPI_E_INVALID_PARAMETER из метода [IMAPITable::SortTable.](imapitable-sorttable.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Microsoft Exchange Server протоколы.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папок.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает допустимые операции для основных объектов таблицы.
    
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

