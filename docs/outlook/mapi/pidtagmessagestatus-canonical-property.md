---
title: Каноническое свойство PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355722"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Каноническое свойство PidTagMessageStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит 32-битовую битовуюmask флагов, которая определяет состояние сообщения в таблице содержимого. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MSG_STATUS  <br/> |
|Идентификатор:  <br/> |0x0E17  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Сообщение может существовать в таблице содержимого и в одной или нескольких таблицах результатов поиска, а каждый экземпляр сообщения может иметь разное состояние. Это свойство не должно считаться свойством сообщения, а столбцом в таблице содержимого. 
  
Клиентские приложения могут установить один или несколько из следующих флагов в этом свойстве: 
  
MSGSTATUS_ANSWERED 
  
> На сообщение был ответ. 
    
MSGSTATUS_DELMARKED 
  
> Сообщение помечено для последующего удаления. 
    
MSGSTATUS_DRAFT 
  
> Сообщение находится в состоянии черновика редакции. 
    
MSGSTATUS_HIDDEN 
  
> Сообщение должно быть отобрачено из папки получателей. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Сообщение должно быть выделено в папке получателей. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Сообщение помечено для удаления в удаленном хранилище сообщений без загрузки в локальный клиент. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Сообщение помечено для скачивания из удаленного хранения сообщений в локальный клиент. 
    
MSGSTATUS_TAGGED 
  
> Сообщение помечено для определенной клиентом цели.
    
Флаги **MSGSTATUS_DELMARKED,** **MSGSTATUS_HIDDEN,** **MSGSTATUS_HIGHLIGHTED** и MSGSTATUS_TAGGED определяются  клиентом. Поставщики транспорта и хранения передают эти биты без каких-либо действий. 
  
Клиенты могут интерпретировать эти значения любым способом, который подходит для их приложений. Один из способов использования этого свойства многими клиентами — отображение сообщений, помеченных для удаления с помощью символьного значка. 
  
Клиент удаленного просмотра  может MSGSTATUS_REMOTE_DELETE или **MSGSTATUS_REMOTE_DOWNLOAD** для сообщений в папке header, представляемой ему поставщиком удаленного транспорта. Клиентские приложения могут проверять каждый заголок сообщений в этой папке, чтобы определить, следует ли скачивать или удалять сообщение в удаленном хранилище сообщений. Затем он использует метод [IMAPIFolder::SetMessageStatus,](imapifolder-setmessagestatus.md) чтобы установить соответствующий флаг. **SetMessageStatus** — единственный способ установить любой из флагов в этом свойстве; Невозможно [использовать метод IMAPIProp::SetProps.](imapiprop-setprops.md) Чтобы получить это свойство, клиенты вызывают [IMAPIFolder::GetMessageStatus,](imapifolder-getmessagestatus.md) а [не IMAPIProp::GetProps.](imapiprop-getprops.md)
  
Биты от 16 до 31 (0x10000 0x80000000) этого свойства доступны для использования клиентского приложения IPM. Все остальные биты зарезервированы для использования в MAPI; те, которые не определены в предыдущей таблице, должны изначально иметь нулевое значение и не изменяться в дальнейшем. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

