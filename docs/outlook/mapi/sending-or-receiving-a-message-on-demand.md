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
ms.openlocfilehash: 668e1c57c59bf2356be808e0347e1bd5135478a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563893"
---
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="d4f70-103">Отправки и получения сообщений по запросу</span><span class="sxs-lookup"><span data-stu-id="d4f70-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="d4f70-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4f70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4f70-105">Клиенты обычно используют подсистемы MAPI — диспетчер очереди MAPI и поставщиков услуг — обработка время передачи сообщений и прием.</span><span class="sxs-lookup"><span data-stu-id="d4f70-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="d4f70-106">Тем не менее можно изменить это время с помощью объекта состояние очереди MAPI или поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d4f70-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="d4f70-107">Метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) удаляет все сообщения из одного или нескольких транспорта поставщика входящих или исходящих очередей.</span><span class="sxs-lookup"><span data-stu-id="d4f70-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="d4f70-108">Следующие процедуры описывают два способа для отправки и получения сообщений по запросу.</span><span class="sxs-lookup"><span data-stu-id="d4f70-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="d4f70-109">Первый процедуре используется объект состояния очереди MAPI для очистки в очереди для каждого поставщика транспорта в профиле; во второй процедуре очищает очереди поставщик единого транспорта.</span><span class="sxs-lookup"><span data-stu-id="d4f70-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="d4f70-110">Для очистки всех входящих или исходящих очередей за одну операцию</span><span class="sxs-lookup"><span data-stu-id="d4f70-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="d4f70-111">Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="d4f70-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="d4f70-112">Вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблице состояния для ограничения в столбце, задайте значение **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d4f70-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="d4f70-113">Выполните построение ограничение свойства, с помощью структуры [SPropertyRestriction](spropertyrestriction.md) в соответствии с **PR_RESOURCE_TYPE** с MAPI_SPOOLER.</span><span class="sxs-lookup"><span data-stu-id="d4f70-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="d4f70-114">Вызовите [HrQueryAllRows](hrqueryallrows.md), передав в структуре **SPropertyRestriction** , чтобы получить строку, представляющую состояние очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="d4f70-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="d4f70-115">Передайте в столбце **PR_ENTRYID** [IMAPISession::OpenEntry](imapisession-openentry.md) , чтобы открыть диспетчер очереди MAPI состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d4f70-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="d4f70-116">Вызовите метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) диспетчер очереди MAPI, передав флаг FLUSH_NO_UI для отмены вывода пользовательского интерфейса и FLUSH_DOWNLOAD или FLUSH_UPLOAD флаг Очистка очереди входящих или исходящих.</span><span class="sxs-lookup"><span data-stu-id="d4f70-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="d4f70-117">Освобождение состояние объекта и в таблице состояния, а также структура [SRowSet](srowset.md) , выделяемый для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4f70-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="d4f70-118">Очистка очереди входящих или исходящих по отдельности, поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="d4f70-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="d4f70-119">Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="d4f70-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="d4f70-120">Вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблице состояния для ограничения в столбце, задайте для **PR_ENTRYID** и **PR_RESOURCE_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="d4f70-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="d4f70-121">Выполните построение ограничение свойства, с помощью структуры [SPropertyRestriction](spropertyrestriction.md) в соответствии с **PR_RESOURCE_TYPE** с MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="d4f70-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="d4f70-122">Вызовите [HrQueryAllRows](hrqueryallrows.md), передав в структуре **SPropertyRestriction** для извлечения строк, поставляемые поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="d4f70-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="d4f70-123">Для каждой строки, возвращаемой из **HrQueryAllRows**:</span><span class="sxs-lookup"><span data-stu-id="d4f70-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="d4f70-124">Передайте в столбце **PR_ENTRYID** [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия объект состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d4f70-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="d4f70-125">Проверьте, что объект состояния транспорта поддерживает метод **FlushQueues** , проверьте, что его свойство **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) имеет STATUS_FLUSH_QUEUES помечает set.</span><span class="sxs-lookup"><span data-stu-id="d4f70-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="d4f70-126">Если поддерживается, вызовите [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span><span class="sxs-lookup"><span data-stu-id="d4f70-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="d4f70-127">Если не поддерживается, вызовите метод **IMAPIStatus::FlushQueues** диспетчер очереди MAPI, передав идентификатор записи транспорта с помощью параметра _lpTargetTransport_ .</span><span class="sxs-lookup"><span data-stu-id="d4f70-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="d4f70-128">Просмотрите и предыдущая процедура для получения инструкций на доступ к объектам состояние очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="d4f70-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="d4f70-129">Значение флага FLUSH_DOWNLOAD Очистка очереди исходящих сообщений или флаг FLUSH_UPLOAD Очистка входящей очереди.</span><span class="sxs-lookup"><span data-stu-id="d4f70-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="d4f70-130">Освобождение состояние объекта и в таблице состояния, а также структура [SRowSet](srowset.md) , выделяемый для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4f70-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="d4f70-131">Диспетчер очереди MAPI учитывает флаг FLUSH_NO_UI, как большинство поставщиков транспорта локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4f70-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="d4f70-132">Тем не менее не все поставщики транспорта поддерживать этот флаг, особенно тех, которые явно использовать модем и служба удаленного доступа (RAS).</span><span class="sxs-lookup"><span data-stu-id="d4f70-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="d4f70-133">Чтобы разрешить клиентам для подавления пользовательского интерфейса не использовался удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="d4f70-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="d4f70-134">Существует возможность клиент мог настроить таким образом, может подключиться без установки основных сборок взаимодействия пользователя, но трудно и требуется обновить знания клиента службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d4f70-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

