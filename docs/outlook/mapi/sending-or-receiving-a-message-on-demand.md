---
title: Отправки и получения сообщений по запросу
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ece5340497f83862b711f076c8c6346e14ec9355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812252"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Отправки и получения сообщений по запросу
  
**Относится к**: Outlook 
  
Клиенты обычно используют подсистемы MAPI — диспетчер очереди MAPI и поставщиков услуг — обработка время передачи сообщений и прием. Тем не менее можно изменить это время с помощью объекта состояние очереди MAPI или поставщика транспорта.
  
Метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) удаляет все сообщения из одного или нескольких транспорта поставщика входящих или исходящих очередей. Следующие процедуры описывают два способа для отправки и получения сообщений по запросу. Первый процедуре используется объект состояния очереди MAPI для очистки в очереди для каждого поставщика транспорта в профиле; во второй процедуре очищает очереди поставщик единого транспорта. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Для очистки всех входящих или исходящих очередей за одну операцию
  
1. Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблице состояния для ограничения в столбце, задайте значение **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Выполните построение ограничение свойства, с помощью структуры [SPropertyRestriction](spropertyrestriction.md) в соответствии с **PR_RESOURCE_TYPE** с MAPI_SPOOLER. 
    
4. Вызовите [HrQueryAllRows](hrqueryallrows.md), передав в структуре **SPropertyRestriction** , чтобы получить строку, представляющую состояние очереди MAPI. 
    
5. Передайте в столбце **PR_ENTRYID** [IMAPISession::OpenEntry](imapisession-openentry.md) , чтобы открыть диспетчер очереди MAPI состояние объекта. 
    
6. Вызовите метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) диспетчер очереди MAPI, передав флаг FLUSH_NO_UI для отмены вывода пользовательского интерфейса и FLUSH_DOWNLOAD или FLUSH_UPLOAD флаг Очистка очереди входящих или исходящих. 
    
7. Освобождение состояние объекта и в таблице состояния, а также структура [SRowSet](srowset.md) , выделяемый для таблицы. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Очистка очереди входящих или исходящих по отдельности, поставщика транспорта
  
1. Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблице состояния для ограничения в столбце, задайте для **PR_ENTRYID** и **PR_RESOURCE_TYPE**.
    
3. Выполните построение ограничение свойства, с помощью структуры [SPropertyRestriction](spropertyrestriction.md) в соответствии с **PR_RESOURCE_TYPE** с MAPI_TRANSPORT_PROVIDER. 
    
4. Вызовите [HrQueryAllRows](hrqueryallrows.md), передав в структуре **SPropertyRestriction** для извлечения строк, поставляемые поставщиками транспорта. 
    
5. Для каждой строки, возвращаемой из **HrQueryAllRows**:
    
    1. Передайте в столбце **PR_ENTRYID** [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия объект состояние поставщика транспорта. 
        
    2. Проверьте, что объект состояния транспорта поддерживает метод **FlushQueues** , проверьте, что его свойство **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) имеет STATUS_FLUSH_QUEUES помечает set. 
        
    3. Если поддерживается, вызовите [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Если не поддерживается, вызовите метод **IMAPIStatus::FlushQueues** диспетчер очереди MAPI, передав идентификатор записи транспорта с помощью параметра _lpTargetTransport_ . Просмотрите и предыдущая процедура для получения инструкций на доступ к объектам состояние очереди MAPI. Значение флага FLUSH_DOWNLOAD Очистка очереди исходящих сообщений или флаг FLUSH_UPLOAD Очистка входящей очереди. 
        
    4. Освобождение состояние объекта и в таблице состояния, а также структура [SRowSet](srowset.md) , выделяемый для таблицы. 
    
Диспетчер очереди MAPI учитывает флаг FLUSH_NO_UI, как большинство поставщиков транспорта локальной сети. Тем не менее не все поставщики транспорта поддерживать этот флаг, особенно тех, которые явно использовать модем и служба удаленного доступа (RAS). Чтобы разрешить клиентам для подавления пользовательского интерфейса не использовался удаленного доступа. Существует возможность клиент мог настроить таким образом, может подключиться без установки основных сборок взаимодействия пользователя, но трудно и требуется обновить знания клиента службы сообщений.
  

