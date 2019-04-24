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
  
Содержит количество непрочитанных сообщений в папке, вычисленное хранилищем сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_КОНТЕНТ_УНРЕАД  <br/> |
|Идентификатор:  <br/> |0x3603  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство, вычисляемое хранилищем сообщений, используется для двух различных, но связанных целей. На объекте папки MAPI он содержит количество сообщений в папке. В строке заголовков в таблицах MAPI с классификацией она содержит число несвязанных сообщений в категории, соответствующей строке заголовков.
  
Данное свойство содержит количество сообщений в таблице содержимого папки, для которых не задан флаг МСГФЛАГ_РЕАД в свойстве **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Свойство **пр_контент_каунт** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) содержит общее количество сообщений для папки. **Пр_контент_каунт** и это свойство доступны только для чтения клиентам. 
  
Некоторые клиентские приложения отображают строку заголовка категории по-разному в зависимости от значения этого свойства. Например, клиент может отобразить категорию, включающую непрочитанные сообщения полужирным шрифтом. Это свойство нельзя использовать в качестве категории, и при попытке сделать это будет получено значение МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР, возвращаемое методом [IMAPITable:: сорттабле](imapitable-sorttable.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Microsoft Exchange Server.
    
[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
[[MS — ОКСКТАБЛ]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает в себя допустимые операции для основных объектов Table.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

