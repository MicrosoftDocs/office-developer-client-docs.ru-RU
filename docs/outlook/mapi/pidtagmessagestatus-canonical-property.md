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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382808"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Каноническое свойство PidTagMessageStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит 32-разрядная версия битовую маску флагов, который определяет состояние сообщения в таблице содержимое. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MSG_STATUS  <br/> |
|Идентификатор:  <br/> |0x0E17  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Сообщения могут существовать в таблицу содержимого и в одной или нескольких таблиц результатов поиска, и каждый экземпляр сообщение может иметь другое состояние. Это свойство не следует считать свойства на сообщение, но на столбец в таблице содержимое. 
  
Клиентское приложение можно установить одно или несколько из следующих флагов в этом свойстве. 
  
MSGSTATUS_ANSWERED 
  
> Сообщение был отправлен ответ. 
    
MSGSTATUS_DELMARKED 
  
> Сообщение было помечено для последующего удаления. 
    
MSGSTATUS_DRAFT 
  
> Сообщение находится в статус черновой версии. 
    
MSGSTATUS_HIDDEN 
  
> Сообщение является должны быть отключены от получателей папке отображается. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Сообщение будет выделена в папке отображается получателей. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Сообщение было помечено для удаления в магазине удаленных сообщений без загрузки локального клиента. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Сообщение было помечено для загрузки с хранения удаленных сообщений для локального клиента. 
    
MSGSTATUS_TAGGED 
  
> Сообщение уже помечен для определенного клиента цели.
    
Флаги **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**и **MSGSTATUS_TAGGED** определяются клиента. Поставщики транспорта и хранилища передайте эти биты без каких-либо действий. 
  
Клиенты могут интерпретировать эти значения никаких уведомлений, подходящую для своих приложений. Для отображения сообщения, помеченные для удаления со значком пример является одним из способов, что количество клиентов использовать это свойство. 
  
Средство просмотра удаленных клиентов можно установить **MSGSTATUS_REMOTE_DELETE** или **MSGSTATUS_REMOTE_DOWNLOAD** для сообщений в папке заголовок, предоставленных поставщиком удаленного транспорта. Клиентское приложение может проверить заголовок каждого сообщения в эту папку, чтобы определить загружен или удаляются, хранения удаленных сообщений сообщения. Он используется метод [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) установить соответствующий флаг. **SetMessageStatus** — это единственный способ задайте флаги в этого свойства. метод [IMAPIProp::SetProps](imapiprop-setprops.md) не может использоваться. Для получения этого свойства, клиенты вызывать [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) , а не [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Бит 16 до 31 (0x10000 через 0x80000000) этого свойства доступны для использования клиентским приложением электронной почты — это сообщение (IPM). Все другие биты, зарезервированы для использования с MAPI; не определенных в предыдущей таблице следует сначала задать нулевое значение и не изменить в дальнейшем. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

