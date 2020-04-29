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
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="ccbd5-103">Отправка или получение сообщения по запросу</span><span class="sxs-lookup"><span data-stu-id="ccbd5-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="ccbd5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccbd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccbd5-105">Обычно клиенты используют подсистему MAPI — Диспетчер очереди MAPI и поставщики услуг — для обработки времени передачи и приема сообщений.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="ccbd5-106">Однако это время можно изменить с помощью объекта Status либо из диспетчера MAPI, либо из поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="ccbd5-107">Метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md) удаляет все сообщения из одной или нескольких входящих и исходящих очередей поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="ccbd5-108">В следующих процедурах описываются два способа отправки и получения сообщений по требованию.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="ccbd5-109">В первой процедуре используется объект Status диспетчера MAPI для очистки очередей каждого поставщика транспорта в профиле; во второй процедуре выполняется очистка очереди одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="ccbd5-110">Очистка всех входящих и исходящих очередей в одной операции</span><span class="sxs-lookup"><span data-stu-id="ccbd5-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="ccbd5-111">Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="ccbd5-112">Вызовите для таблицы состояний метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы ограничить набор столбцов значением **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ccbd5-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="ccbd5-113">Создание ограничения свойства с помощью структуры [спропертирестриктион](spropertyrestriction.md) для сравнения **PR_RESOURCE_TYPE** с MAPI_SPOOLER.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="ccbd5-114">Вызовите [хркуеряллровс](hrqueryallrows.md), передав структуру **спропертирестриктион** , чтобы получить строку, представляющую состояние диспетчера очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="ccbd5-115">Передайте столбец **PR_ENTRYID** в [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть объект состояния диспетчера MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="ccbd5-116">Вызовите метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md) ДИСПЕТЧЕРА очереди MAPI, передав флаг FLUSH_NO_UI, чтобы запретить пользовательский интерфейс, а также флаг FLUSH_DOWNLOAD или FLUSH_UPLOAD для очистки исходящих или входящих очередей.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="ccbd5-117">Отпустите объект status и таблицу status, а также структуру [SRowSet](srowset.md) , выделенную для таблицы.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="ccbd5-118">Очистка входящих и исходящих очередей по отдельности с помощью поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="ccbd5-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="ccbd5-119">Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="ccbd5-120">Вызовите таблицу состояния [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы ограничить набор столбцов значением **PR_ENTRYID** и **PR_RESOURCE_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="ccbd5-121">Создание ограничения свойства с помощью структуры [спропертирестриктион](spropertyrestriction.md) для сравнения **PR_RESOURCE_TYPE** с MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="ccbd5-122">Вызовите [хркуеряллровс](hrqueryallrows.md), передав структуру **спропертирестриктион** , чтобы получить строки, предоставляемые поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="ccbd5-123">Для каждой строки, возвращаемой из **хркуеряллровс**:</span><span class="sxs-lookup"><span data-stu-id="ccbd5-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="ccbd5-124">Передайте столбец **PR_ENTRYID** в [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть объект состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="ccbd5-125">Убедитесь, что объект состояния транспорта поддерживает метод **FlushQueues** , проверив, установлен ли для свойства **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) флаг STATUS_FLUSH_QUEUES.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="ccbd5-126">Если он поддерживается, вызовите метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md).</span><span class="sxs-lookup"><span data-stu-id="ccbd5-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="ccbd5-127">Если этот параметр не поддерживается, вызовите метод **имапистатус:: FlushQueues** диспетчера MAPI, передав идентификатор записи транспорта в параметр _лптаржеттранспорт_ .</span><span class="sxs-lookup"><span data-stu-id="ccbd5-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="ccbd5-128">Инструкции по доступу к объекту Status диспетчера MAPI приведены в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="ccbd5-129">Установите флаг FLUSH_DOWNLOAD для очистки исходящих очередей или флага FLUSH_UPLOAD для очистки входящих очередей.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="ccbd5-130">Отпустите объект status и таблицу status, а также структуру [SRowSet](srowset.md) , выделенную для таблицы.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="ccbd5-131">Диспетчер очереди MAPI учитывает FLUSH_NO_UI флаг как большинство поставщиков транспорта ЛВС.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="ccbd5-132">Однако не все поставщики транспорта учитывают этот флаг, особенно те, которые используют модем явным образом и служба удаленного доступа (RAS).</span><span class="sxs-lookup"><span data-stu-id="ccbd5-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="ccbd5-133">Служба удаленного доступа не была разработана, чтобы запретить клиентам отключать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="ccbd5-134">Клиент может быть настроен таким образом, чтобы он мог подключаться без взаимодействия с пользователем, но это очень сложно и требует хорошо знать службы сообщений клиента.</span><span class="sxs-lookup"><span data-stu-id="ccbd5-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

