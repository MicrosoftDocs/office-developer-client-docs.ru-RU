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
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360783"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Каноническое свойство PidTagDisplayType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, используемого для связи значка с определенной строкой таблицы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Идентификатор:  <br/> |0x3900  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит длинный набор, который облегчает специальную обработку записи таблицы в зависимости от ее типа. Это специальное лечение обычно состоит из отображения значка или другого элемента отображения, связанного с типом отображения. 
  
Это свойство не используется в таблицах содержимого папок. Клиентские приложения должны использовать свойство **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)и соответствующий интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) для получения свойств **PR_ICON** [(PidTagIcon)](pidtagicon-canonical-property.md)и **PR_MINI_ICON** [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md) 
  
Это свойство может иметь одно из следующих значений:
  
DT_AGENT 
  
> Автоматический агент, например Quote-Of-The-Day или отображение диаграммы погоды.
    
DT_DISTLIST 
  
> Список рассылки.
    
DT_FOLDER 
  
> Отображение значка папки по умолчанию рядом с папкой.
    
DT_FOLDER_LINK 
  
> Отображение значка ссылки папки по умолчанию рядом с папкой, а не значком папки по умолчанию.
    
DT_FOLDER_SPECIAL 
  
> Отображение значка для папки с различиями, определенными приложениями, такими как специальный тип общедоступных папок.
    
DT_FORUM 
  
> Форум, например служба доски объявлений, публичная или общая папка.
    
DT_GLOBAL 
  
> Глобальная адресная книга.
    
DT_LOCAL 
  
> Локализованная адресная книга, которую вы делитесь с небольшой группы.
    
DT_MAILUSER 
  
> Типичный пользователь обмена сообщениями.
    
DT_MODIFIABLE 
  
> Модификабель; контейнер должен быть обозначаться как модификабельный в пользовательском интерфейсе.
    
DT_NOT_SPECIFIC 
  
> Не соответствует другим настройкам.
    
DT_ORGANIZATION 
  
> Специальный псевдоним, определенный для большой группы, например helpdesk, accounting или blood-drive coordinator.
    
DT_PRIVATE_DISTLIST 
  
> Частный, лично управляемый список рассылки.
    
DT_REMOTE_MAILUSER 
  
> Получатель, как известно, из иностранной или удаленной системы обмена сообщениями.
    
DT_WAN 
  
> Широкая адресная книга сетевой сети.
    
В таблицах контента адресной книги используются значения DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST и DT_REMOTE_MAILUSER. Таблицы иерархии адресных книг и разовые таблицы используют значения DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC и DT_WAN. Таблицы иерархии папок используют значения DT_FOLDER, DT_FOLDER_LINK и DT_FOLDER_SPECIAL. 
  
Если это свойство не установлено, клиент должен считать тип по умолчанию подходящим для таблицы, как правило, DT_FOLDER, DT_LOCAL или DT_MAILUSER. 
  
 **Примечание** Все значения, не задокументированные, зарезервированы для MAPI. Клиентские приложения не должны определять новые значения и должны быть готовы к обращению с недокументным значением. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для шаблонов адресной книги.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Включает доступ к каталогам.
    
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

