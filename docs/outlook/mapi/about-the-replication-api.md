---
title: Сведения об API репликации
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 50b36ee60d00e06a1f5baa8726b5f27c4a3e6ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807974"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="f5a33-103">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="f5a33-103">About the Replication API</span></span>

  
  
<span data-ttu-id="f5a33-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5a33-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5a33-105">Интерфейс API репликации предоставляет функциональные возможности для поставщика хранилища сообщений MAPI для синхронизации элементов Microsoft Outlook 2013 или Microsoft Outlook 2010 между сервером и закрытый на основе .pst локального хранилища, созданный для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5a33-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f5a33-106">Поставщик хранения сообщений MAPI необходимо реализовать API репликации согласно инструкциям в [О конечного автомата репликации](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="f5a33-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="f5a33-107">Поставщик должен использовать API-Интерфейс только на личном хранилище, созданные для самого, а не на личные хранилища, созданные для других поставщиков, так как для создания личных хранилищ других поставщиков уже настроить собственные механизма репликации с соответствующими сервером.</span><span class="sxs-lookup"><span data-stu-id="f5a33-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="f5a33-108">Например файл автономной папки (OST) поддерживает собственный репликации отношения с Microsoft Exchange server.</span><span class="sxs-lookup"><span data-stu-id="f5a33-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="f5a33-109">Чтобы использовать API репликации, поставщика хранилища сообщений MAPI сначала необходимо открыть и перенос локального хранилища на основе .pst путем вызова **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="f5a33-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="f5a33-110">Поставщик затем можно использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)**, чтобы выполнить репликацию.</span><span class="sxs-lookup"><span data-stu-id="f5a33-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="f5a33-111">**IPSTX** предоставляется с помощью запроса на [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), и **IOSTX** обеспечивается **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="f5a33-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="f5a33-112">Интерфейс IOSTX</span><span class="sxs-lookup"><span data-stu-id="f5a33-112">The IOSTX Interface</span></span>

<span data-ttu-id="f5a33-113">Интерфейс **IOSTX** — это основной интерфейс, который выполняет синхронизацию в API репликации.</span><span class="sxs-lookup"><span data-stu-id="f5a33-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="f5a33-114">**IOSTX** перемещает локального хранилища ряд состояний, получение сведений об изменениях в локальном хранилище каждого состояния, а также о том, локального хранилища изменения на сервере.</span><span class="sxs-lookup"><span data-stu-id="f5a33-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="f5a33-115">API репликации также приведены несколько структур данных, которые поддерживают синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="f5a33-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="f5a33-116">Поставщик хранения, как клиент этот интерфейс API использует API репликации для переноса локального хранилища и перемещаться по эти состояния принудительную изменений в локальном хранилище (например, изменения иерархии папок или добавление новых элементов) на сервер, а также извлечение сведения об изменениях на сервере и предоставляя эти сведения об интерфейсе **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="f5a33-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="f5a33-117">Интерфейс **IOSTX** принимает добавочные изменения синхронизации (ICS) предоставлено Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f5a33-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="f5a33-118">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="f5a33-118">For more information about ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="f5a33-119">Через **IOSTX**клиент использует ICS для мониторинга и синхронизировать добавочные изменения иерархии или контента для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="f5a33-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="f5a33-120">Интерфейс IPSTX</span><span class="sxs-lookup"><span data-stu-id="f5a33-120">The IPSTX Interface</span></span>

 <span data-ttu-id="f5a33-121">**IPSTX** и пять других ** IPSTX *n* ** интерфейсы, производные от **IPSTX** предоставляют функциональные возможности модуля поддержки, который можно использовать при выполнении репликации с помощью интерфейса **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="f5a33-121">**IPSTX** and five other **IPSTX *n* ** interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="f5a33-122">Например **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** позволяет сделать локального хранилища эмуляции диспетчера протокола Outlook очереди исходящих сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="f5a33-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="f5a33-123">Дополнительные сведения о переходы между состояниями во время репликации можно [О конечного автомата репликации](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="f5a33-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="f5a33-124">Интерфейс API репликации</span><span class="sxs-lookup"><span data-stu-id="f5a33-124">The Replication API</span></span>

<span data-ttu-id="f5a33-125">API репликации предоставляет файлов определения, типы данных и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f5a33-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="f5a33-126">Пример реализации поставщика хранилища для оболочку файлы личных папок (PST) в разделе [О пример оболочку PST поставщика хранилища](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f5a33-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="f5a33-127">Определения:</span><span class="sxs-lookup"><span data-stu-id="f5a33-127">Definitions:</span></span>
  
- [<span data-ttu-id="f5a33-128">Константы для репликации API</span><span class="sxs-lookup"><span data-stu-id="f5a33-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="f5a33-129">Функции:</span><span class="sxs-lookup"><span data-stu-id="f5a33-129">Functions:</span></span>
  
- <span data-ttu-id="f5a33-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="f5a33-131">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="f5a33-131">Data types:</span></span>
  
- <span data-ttu-id="f5a33-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="f5a33-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="f5a33-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="f5a33-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="f5a33-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="f5a33-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="f5a33-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="f5a33-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="f5a33-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="f5a33-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="f5a33-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="f5a33-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="f5a33-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="f5a33-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="f5a33-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="f5a33-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="f5a33-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="f5a33-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="f5a33-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="f5a33-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="f5a33-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="f5a33-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="f5a33-154">Интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="f5a33-154">Interfaces:</span></span>
  
- <span data-ttu-id="f5a33-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="f5a33-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="f5a33-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="f5a33-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="f5a33-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="f5a33-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="f5a33-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a33-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

