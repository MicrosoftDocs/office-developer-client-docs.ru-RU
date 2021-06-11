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
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="7299f-103">Отправка или получение сообщения по запросу</span><span class="sxs-lookup"><span data-stu-id="7299f-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="7299f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7299f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7299f-105">Клиенты обычно полагаются на подсистему MAPI — шпалер MAPI и поставщиков услуг — для обработки сроков передачи и приема сообщений.</span><span class="sxs-lookup"><span data-stu-id="7299f-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="7299f-106">Однако эти сроки можно изменить, используя объект состояния как шпалер MAPI, так и поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="7299f-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="7299f-107">Метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) удаляет все сообщения из входящих или исходяющих очередей поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="7299f-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="7299f-108">В следующих процедурах описаны два метода отправки или получения сообщений по запросу.</span><span class="sxs-lookup"><span data-stu-id="7299f-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="7299f-109">Первая процедура использует объект состояния spooler MAPI для очистки очередей каждого поставщика транспорта в профиле; вторая процедура смыва очереди одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="7299f-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="7299f-110">Очистка всех входящих или исходяющих очередей в одной операции</span><span class="sxs-lookup"><span data-stu-id="7299f-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="7299f-111">Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="7299f-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="7299f-112">Позвоните в [IMAPITable таблицы состояния:::SetColumns,](imapitable-setcolumns.md)  чтобы ограничить значение столбца PR_ENTRYID [(PidTagEntryId)](pidtagentryid-canonical-property.md)и **PR_RESOURCE_TYPE** [(PidTagResourceType).](pidtagresourcetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7299f-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="7299f-113">Создайте ограничение свойств с помощью [структуры SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать PR_RESOURCE_TYPE **с** MAPI_SPOOLER.</span><span class="sxs-lookup"><span data-stu-id="7299f-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="7299f-114">[Вызывай hrQueryAllRows,](hrqueryallrows.md)передав структуру **SPropertyRestriction,** чтобы получить строку, представляюную состояние пулера MAPI.</span><span class="sxs-lookup"><span data-stu-id="7299f-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="7299f-115">**Передай столбец** PR_ENTRYID [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть объект состояния пульпера MAPI.</span><span class="sxs-lookup"><span data-stu-id="7299f-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="7299f-116">Вызовите метод [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) передав флаг FLUSH_NO_UI, чтобы подавить пользовательский интерфейс и флаг FLUSH_DOWNLOAD или FLUSH_UPLOAD, чтобы смыть исходящую или входящую очередь.</span><span class="sxs-lookup"><span data-stu-id="7299f-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="7299f-117">Отпустите объект состояния и таблицу состояния, а также структуру [SRowSet,](srowset.md) выделенную для таблицы.</span><span class="sxs-lookup"><span data-stu-id="7299f-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="7299f-118">Для очистки входящих или исходяющих очередей по отдельности поставщиком транспорта</span><span class="sxs-lookup"><span data-stu-id="7299f-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="7299f-119">Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="7299f-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="7299f-120">Вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы состояния, чтобы  ограничить набор столбцов PR_ENTRYID **и PR_RESOURCE_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="7299f-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="7299f-121">Создайте ограничение свойств с помощью [структуры SPropertyRestriction,](spropertyrestriction.md) чтобы соответствовать PR_RESOURCE_TYPE **с** MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="7299f-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="7299f-122">Вызов [HrQueryAllRows,](hrqueryallrows.md)проходящий в **структуре SPropertyRestriction,** чтобы получить строки, которые поставляются поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="7299f-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="7299f-123">Для каждой строки, возвращаемой **из HrQueryAllRows:**</span><span class="sxs-lookup"><span data-stu-id="7299f-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="7299f-124">**Передай столбец** PR_ENTRYID [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть объект состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="7299f-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="7299f-125">Убедитесь, что объект состояния транспорта поддерживает метод **FlushQueues,** **проверяя,** что его свойство [PR_RESOURCE_METHODS (PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)имеет STATUS_FLUSH_QUEUES флага.</span><span class="sxs-lookup"><span data-stu-id="7299f-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="7299f-126">Если поддерживается, позвоните [в IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span><span class="sxs-lookup"><span data-stu-id="7299f-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="7299f-127">Если неподдерживаемая, позвоните по методу **IMAPIStatus::FlushQueues,** передав идентификатор входа транспорта в _параметре lpTargetTransport._</span><span class="sxs-lookup"><span data-stu-id="7299f-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="7299f-128">См. предшествую процедуру инструкций по доступу к объекту состояния пульпера MAPI.</span><span class="sxs-lookup"><span data-stu-id="7299f-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="7299f-129">Установите флаг FLUSH_DOWNLOAD, чтобы смыть исходящую очередь или флаг FLUSH_UPLOAD, чтобы смыть входящие очереди.</span><span class="sxs-lookup"><span data-stu-id="7299f-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="7299f-130">Отпустите объект состояния и таблицу состояния, а также структуру [SRowSet,](srowset.md) выделенную для таблицы.</span><span class="sxs-lookup"><span data-stu-id="7299f-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="7299f-131">Шпалер MAPI почитает флаг FLUSH_NO_UI, как и большинство поставщиков lan-транспорта.</span><span class="sxs-lookup"><span data-stu-id="7299f-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="7299f-132">Однако не все поставщики транспорта чтят этот флаг, особенно те, которые явно используют модем и службу удаленного доступа (RAS).</span><span class="sxs-lookup"><span data-stu-id="7299f-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="7299f-133">RaS не предназначен для того, чтобы позволить клиентам подавить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7299f-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="7299f-134">Клиент может быть настроен таким образом, что он может подключаться, не требуя взаимодействия пользователя, но это сложно и требует интимных знаний о службах сообщений клиента.</span><span class="sxs-lookup"><span data-stu-id="7299f-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

