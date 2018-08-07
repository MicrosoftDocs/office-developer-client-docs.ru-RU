---
title: Каноническое свойство PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3fd5a8d92621dcefce66fb42e843f78755fa84df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811084"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Каноническое свойство PidTagDisplayType

  
  
**Относится к**: Outlook 
  
Содержит значение, используемое для сопоставления значка с конкретной строки таблицы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Идентификатор:  <br/> |0x3900  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит длинное целое, которая упрощает специальная обработка записи таблицы, на основе этого типа. Эта специальная обработка обычно состоит из отображения значка или других отображения элемента, связанного с типа отображения. 
  
Это свойство не используется в таблицах содержимое папки. Для получения **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) и **PR_MINI_ICON** ([ клиентских приложений следует использовать свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) и соответствующий интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) сообщения PidTagMiniIcon](pidtagminiicon-canonical-property.md)) свойства для этого сообщения. 
  
Это свойство может иметь только один из следующих значений:
  
DT_AGENT 
  
> Автоматическая отправка агента, такие как квоты день или отображение диаграмм прогноза погоды.
    
DT_DISTLIST 
  
> Список рассылки.
    
DT_FOLDER 
  
> Отображение значка папки по умолчанию рядом с папки.
    
DT_FOLDER_LINK 
  
> Отображение по умолчанию папки ссылок значок рядом с папки, а не значок папки по умолчанию.
    
DT_FOLDER_SPECIAL 
  
> Отображение значка для папки с различие конкретного приложения, такие как особый тип общей папки.
    
DT_FORUM 
  
> Форум, таких как служба досках или общедоступный или общей папки.
    
DT_GLOBAL 
  
> Глобальной адресной книги.
    
DT_LOCAL 
  
> Локальной адресной книги, совместно с небольшой рабочей группы.
    
DT_MAILUSER 
  
> Обычной пользовательской обмена мгновенными сообщениями.
    
DT_MODIFIABLE 
  
> Можно изменить; контейнер должен идентификаторами как можно изменить в пользовательском интерфейсе.
    
DT_NOT_SPECIFIC 
  
> Не соответствует другие параметры.
    
DT_ORGANIZATION 
  
> Специальные псевдоним, определенных для больших групп, такие как служба технической поддержки, учета или координатора кровь диска.
    
DT_PRIVATE_DISTLIST 
  
> Частный, раскрывающие личность администрировать с помощью списка рассылки.
    
DT_REMOTE_MAILUSER 
  
> Получатель, известно, из внешнего или удаленных систем обмена сообщениями.
    
DT_WAN 
  
> В глобальной сети адресную книгу.
    
Содержимое таблиц адресной книги используются значения DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST и DT_REMOTE_MAILUSER. Используйте значения DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC и DT_WAN в одноразовых таблиц и таблиц иерархии адресной книги. Таблиц иерархии папок используйте значения DT_FOLDER, DT_FOLDER_LINK и DT_FOLDER_SPECIAL. 
  
Если это свойство не задано, клиент должен использовать тип по умолчанию для таблицы, обычно DT_FOLDER, DT_LOCAL или DT_MAILUSER. 
  
 **Примечание** Все значения не задокументирован зарезервированы для MAPI. Клиентские приложения не должны определить все новые значения и должны быть готовы для смягчения последствий недокументированного значения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для шаблонов адресной книги.
    
[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Обеспечивает доступ к каталогу.
    
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

