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
  
Обычно клиенты используют подсистему MAPI — Диспетчер очереди MAPI и поставщики услуг — для обработки времени передачи и приема сообщений. Однако это время можно изменить с помощью объекта Status либо из диспетчера MAPI, либо из поставщика транспорта.
  
Метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md) удаляет все сообщения из одной или нескольких входящих и исходящих очередей поставщика транспорта. В следующих процедурах описываются два способа отправки и получения сообщений по требованию. В первой процедуре используется объект Status диспетчера MAPI для очистки очередей каждого поставщика транспорта в профиле; во второй процедуре выполняется очистка очереди одного поставщика транспорта. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Очистка всех входящих и исходящих очередей в одной операции
  
1. Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Вызовите для таблицы состояний метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы ограничить набор столбцов значением **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Создание ограничения свойства с помощью структуры [спропертирестриктион](spropertyrestriction.md) для сравнения **PR_RESOURCE_TYPE** с MAPI_SPOOLER. 
    
4. Вызовите [хркуеряллровс](hrqueryallrows.md), передав структуру **спропертирестриктион** , чтобы получить строку, представляющую состояние диспетчера очереди MAPI. 
    
5. Передайте столбец **PR_ENTRYID** в [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть объект состояния диспетчера MAPI. 
    
6. Вызовите метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md) ДИСПЕТЧЕРА очереди MAPI, передав флаг FLUSH_NO_UI, чтобы запретить пользовательский интерфейс, а также флаг FLUSH_DOWNLOAD или FLUSH_UPLOAD для очистки исходящих или входящих очередей. 
    
7. Отпустите объект status и таблицу status, а также структуру [SRowSet](srowset.md) , выделенную для таблицы. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Очистка входящих и исходящих очередей по отдельности с помощью поставщика транспорта
  
1. Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Вызовите таблицу состояния [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы ограничить набор столбцов значением **PR_ENTRYID** и **PR_RESOURCE_TYPE**.
    
3. Создание ограничения свойства с помощью структуры [спропертирестриктион](spropertyrestriction.md) для сравнения **PR_RESOURCE_TYPE** с MAPI_TRANSPORT_PROVIDER. 
    
4. Вызовите [хркуеряллровс](hrqueryallrows.md), передав структуру **спропертирестриктион** , чтобы получить строки, предоставляемые поставщиками транспорта. 
    
5. Для каждой строки, возвращаемой из **хркуеряллровс**:
    
    1. Передайте столбец **PR_ENTRYID** в [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть объект состояния поставщика транспорта. 
        
    2. Убедитесь, что объект состояния транспорта поддерживает метод **FlushQueues** , проверив, установлен ли для свойства **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) флаг STATUS_FLUSH_QUEUES. 
        
    3. Если он поддерживается, вызовите метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md). Если этот параметр не поддерживается, вызовите метод **имапистатус:: FlushQueues** диспетчера MAPI, передав идентификатор записи транспорта в параметр _лптаржеттранспорт_ . Инструкции по доступу к объекту Status диспетчера MAPI приведены в предыдущей процедуре. Установите флаг FLUSH_DOWNLOAD для очистки исходящих очередей или флага FLUSH_UPLOAD для очистки входящих очередей. 
        
    4. Отпустите объект status и таблицу status, а также структуру [SRowSet](srowset.md) , выделенную для таблицы. 
    
Диспетчер очереди MAPI учитывает FLUSH_NO_UI флаг как большинство поставщиков транспорта ЛВС. Однако не все поставщики транспорта учитывают этот флаг, особенно те, которые используют модем явным образом и служба удаленного доступа (RAS). Служба удаленного доступа не была разработана, чтобы запретить клиентам отключать пользовательский интерфейс. Клиент может быть настроен таким образом, чтобы он мог подключаться без взаимодействия с пользователем, но это очень сложно и требует хорошо знать службы сообщений клиента.
  

