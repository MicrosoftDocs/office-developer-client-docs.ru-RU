---
title: Отправка или получение сообщения по запросу
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436372"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Отправка или получение сообщения по запросу
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты обычно используют подсистему MAPI (пультер MAPI и поставщиков услуг) для обработки времени передачи и приема сообщений. Однако это время можно изменить с помощью объекта состояния пула MAPI или поставщика транспорта.
  
Метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) удаляет все сообщения из входящих или исходячих очередей одного или более поставщиков транспорта. В следующих процедурах описаны два метода отправки и получения сообщений по запросу. В первой процедуре используется объект состояния пула MAPI для очистки очередей каждого поставщика транспорта в профиле; Вторая процедура очищает очередь одного поставщика транспорта. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Очистка всех входящих и исходяющих очередей за одну операцию
  
1. Вызовите [IMAPISession::GetStatusTable для](imapisession-getstatustable.md) доступа к таблице состояния. 
    
2. Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы состояния, чтобы ограничить значение столбца **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)и **PR_RESOURCE_TYPE** ([PidTagResourceType).](pidtagresourcetype-canonical-property.md)
    
3. Создайте ограничение свойств, используя [структуру SPropertyRestriction](spropertyrestriction.md) для PR_RESOURCE_TYPE **с** MAPI_SPOOLER. 
    
4. Вызовите [HrQueryAllRows,](hrqueryallrows.md)передав структуру **SPropertyRestriction,** чтобы получить строку, представляюную состояние пула MAPI. 
    
5. **Передав столбец PR_ENTRYID** [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть объект состояния пула MAPI. 
    
6. Вызовите метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) пула MAPI, передав флаг FLUSH_NO_UI для подавления пользовательского интерфейса и флаг FLUSH_DOWNLOAD или FLUSH_UPLOAD для очистки исходящую или входящую очередь. 
    
7. Освобождение объекта состояния и таблицы состояния, а также структуры [SRowSet,](srowset.md) выделенной для таблицы. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Очистка входящих и исходяющих очередей по отдельности поставщиком транспорта
  
1. Вызовите [IMAPISession::GetStatusTable для](imapisession-getstatustable.md) доступа к таблице состояния. 
    
2. Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы состояния, чтобы ограничить набор столбцов PR_ENTRYID **и** **PR_RESOURCE_TYPE**.
    
3. Создайте ограничение свойств, используя [структуру SPropertyRestriction](spropertyrestriction.md) **для** PR_RESOURCE_TYPE с MAPI_TRANSPORT_PROVIDER. 
    
4. Вызовите [HrQueryAllRows,](hrqueryallrows.md)передав структуру **SPropertyRestriction,** чтобы получить строки, предоставленные поставщиками транспорта. 
    
5. Для каждой строки, **возвращаемой из HrQueryAllRows:**
    
    1. **Передав столбец PR_ENTRYID** [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть объект состояния поставщика транспорта. 
        
    2. Убедитесь, что объект состояния транспорта поддерживает метод **FlushQueues,** проверив, что его **свойство PR_RESOURCE_METHODS** ([PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)имеет STATUS_FLUSH_QUEUES флага. 
        
    3. Если поддерживается, [вызовите IMAPIStatus::FlushQueues.](imapistatus-flushqueues.md) Если неподдерживаемая, вызовите метод **IMAPIStatus::FlushQueues** пула MAPI, передав идентификатор записи транспорта в _параметре lpTargetTransport._ Инструкции по доступу к объекту состояния пула MAPI см. в предыдущей процедуре. Установите флаг FLUSH_DOWNLOAD для очистки исходяющих очередей или флаг FLUSH_UPLOAD для очистки входящих очередей. 
        
    4. Освобождение объекта состояния и таблицы состояния, а также структуры [SRowSet,](srowset.md) выделенной для таблицы. 
    
В пуле MAPI флаг FLUSH_NO_UI как и большинство поставщиков транспорта локальной сети. Однако не все поставщики транспорта используют этот флаг, особенно те, которые явно используют модем и службу удаленного доступа (RAS). RaS не предназначен для того, чтобы разрешить клиентам подавления пользовательского интерфейса. Клиент может быть настроен таким образом, чтобы он подключался, не требуя взаимодействия с пользователем, но это сложно и требует знаний о службах сообщений клиента.
  

