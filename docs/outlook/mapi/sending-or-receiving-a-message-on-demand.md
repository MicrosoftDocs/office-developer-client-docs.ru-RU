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
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиенты обычно полагаются на подсистему MAPI — шпалер MAPI и поставщиков услуг — для обработки сроков передачи и приема сообщений. Однако эти сроки можно изменить, используя объект состояния как шпалер MAPI, так и поставщик транспорта.
  
Метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) удаляет все сообщения из входящих или исходяющих очередей поставщика транспорта. В следующих процедурах описаны два метода отправки или получения сообщений по запросу. Первая процедура использует объект состояния spooler MAPI для очистки очередей каждого поставщика транспорта в профиле; вторая процедура смыва очереди одного поставщика транспорта. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Очистка всех входящих или исходяющих очередей в одной операции
  
1. Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния. 
    
2. Позвоните в [IMAPITable таблицы состояния:::SetColumns,](imapitable-setcolumns.md)  чтобы ограничить значение столбца PR_ENTRYID [(PidTagEntryId)](pidtagentryid-canonical-property.md)и **PR_RESOURCE_TYPE** [(PidTagResourceType).](pidtagresourcetype-canonical-property.md)
    
3. Создайте ограничение свойств с помощью [структуры SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать PR_RESOURCE_TYPE **с** MAPI_SPOOLER. 
    
4. [Вызывай hrQueryAllRows,](hrqueryallrows.md)передав структуру **SPropertyRestriction,** чтобы получить строку, представляюную состояние пулера MAPI. 
    
5. **Передай столбец** PR_ENTRYID [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть объект состояния пульпера MAPI. 
    
6. Вызовите метод [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) передав флаг FLUSH_NO_UI, чтобы подавить пользовательский интерфейс и флаг FLUSH_DOWNLOAD или FLUSH_UPLOAD, чтобы смыть исходящую или входящую очередь. 
    
7. Отпустите объект состояния и таблицу состояния, а также структуру [SRowSet,](srowset.md) выделенную для таблицы. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Для очистки входящих или исходяющих очередей по отдельности поставщиком транспорта
  
1. Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния. 
    
2. Вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы состояния, чтобы  ограничить набор столбцов PR_ENTRYID **и PR_RESOURCE_TYPE**.
    
3. Создайте ограничение свойств с помощью [структуры SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать PR_RESOURCE_TYPE **с** MAPI_TRANSPORT_PROVIDER. 
    
4. Вызов [HrQueryAllRows,](hrqueryallrows.md)проходящий в **структуре SPropertyRestriction,** чтобы получить строки, которые поставляются поставщиками транспорта. 
    
5. Для каждой строки, возвращаемой **из HrQueryAllRows:**
    
    1. **Передай столбец** PR_ENTRYID [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть объект состояния поставщика транспорта. 
        
    2. Убедитесь, что объект состояния транспорта поддерживает метод **FlushQueues,** **проверяя,** что его свойство [PR_RESOURCE_METHODS (PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)имеет STATUS_FLUSH_QUEUES флага. 
        
    3. Если поддерживается, позвоните [в IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Если неподдерживаемая, позвоните по методу **IMAPIStatus::FlushQueues,** передав идентификатор входа транспорта в _параметре lpTargetTransport._ См. предшествую процедуру инструкций по доступу к объекту состояния пульпера MAPI. Установите флаг FLUSH_DOWNLOAD, чтобы смыть исходящую очередь или флаг FLUSH_UPLOAD, чтобы смыть входящие очереди. 
        
    4. Отпустите объект состояния и таблицу состояния, а также структуру [SRowSet,](srowset.md) выделенную для таблицы. 
    
Шпалер MAPI почитает флаг FLUSH_NO_UI, как и большинство поставщиков lan-транспорта. Однако не все поставщики транспорта чтят этот флаг, особенно те, которые явно используют модем и службу удаленного доступа (RAS). RaS не предназначен для того, чтобы позволить клиентам подавить пользовательский интерфейс. Клиент может быть настроен таким образом, что он может подключаться, не требуя взаимодействия пользователя, но это сложно и требует интимных знаний о службах сообщений клиента.
  

