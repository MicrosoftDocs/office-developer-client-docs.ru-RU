---
title: Сведения об API репликации
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329521"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="4538b-103">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="4538b-103">About the Replication API</span></span>

  
  
<span data-ttu-id="4538b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4538b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4538b-105">API репликации предоставляет функциональные возможности для поставщика хранилища сообщений MAPI, чтобы синхронизировать элементы Microsoft Outlook 2013 или Microsoft Outlook 2010 между сервером и локальным хранилищем на основе PST, созданным для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="4538b-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4538b-106">Поставщик хранилища сообщений MAPI должен реализовать API репликации в соответствии с инструкциями, приведенными в разделе [о конечном автомате репликации](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="4538b-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="4538b-107">Поставщик должен использовать API только в личном хранилище, созданном для самого себя, а не в личных хранилищах, созданных для других поставщиков, так как личные хранилища, созданные для других поставщиков, могут уже настроить собственные механизмы репликации с соответствующим сервером.</span><span class="sxs-lookup"><span data-stu-id="4538b-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="4538b-108">Например, файл автономных папок (OST) поддерживает собственное отношение репликации с сервером Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="4538b-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="4538b-109">Чтобы использовать API репликации, поставщик хранилища сообщений MAPI должен сначала открыть и обернуть локальное хранилище на основе PST, вызвав **[нстсервицеентри](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="4538b-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="4538b-110">Затем поставщик может использовать основные интерфейсы API- **[иосткс](iostxiunknown.md)** и **[ипсткс](ipstxiunknown.md)** для выполнения репликации.</span><span class="sxs-lookup"><span data-stu-id="4538b-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="4538b-111">**Ипсткс** предоставляется с помощью запросов к [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), а **Иосткс** предоставляется **[ипсткс:: жетсинкобжект](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="4538b-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="4538b-112">Интерфейс ИОСТКС</span><span class="sxs-lookup"><span data-stu-id="4538b-112">The IOSTX Interface</span></span>

<span data-ttu-id="4538b-113">Интерфейс **иосткс** — это основной интерфейс, который выполняет синхронизацию в API репликации.</span><span class="sxs-lookup"><span data-stu-id="4538b-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="4538b-114">**Иосткс** перемещает локальное хранилище через ряд состояний, получая сведения об изменениях в локальном хранилище, а также информирует локальное хранилище об изменениях на сервере.</span><span class="sxs-lookup"><span data-stu-id="4538b-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="4538b-115">API репликации также определяет многие структуры данных, которые поддерживают синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="4538b-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="4538b-116">Поставщик магазина, как клиент для этого API, использует API репликации для переноса локального хранилища и перемещения по этим состояниям, отменяя изменения в локальном хранилище (например, изменения в иерархии папок или добавления новых элементов) на сервер, а также получая информацию об изменениях на сервере и предоставляя эту информацию в интерфейс **иосткс** .</span><span class="sxs-lookup"><span data-stu-id="4538b-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="4538b-117">Интерфейс **иосткс** использует добавочную синхронизацию изменений (ICS), предоставляемую Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4538b-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="4538b-118">Дополнительные сведения о ICS приведены в статье [условия оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4538b-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="4538b-119">С помощью **иосткс**клиент использует ICS для отслеживания и синхронизации добавочных изменений в иерархии или контенте в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="4538b-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="4538b-120">Интерфейс ИПСТКС</span><span class="sxs-lookup"><span data-stu-id="4538b-120">The IPSTX Interface</span></span>

 <span data-ttu-id="4538b-121">**Ипсткс** и пять других интерфейсов \* \* ипсткс *n* \* \*, наследуемых от **ипсткс** , предоставляют вспомогательные функции, которые можно использовать при репликации через интерфейс **иосткс** .</span><span class="sxs-lookup"><span data-stu-id="4538b-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="4538b-122">Например, **[ипсткс:: емулатеспулер](ipstx-emulatespooler.md)** позволяет сделать локальное хранилище эмулятором диспетчера протокола Outlook для постановки в очередь исходящих сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="4538b-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="4538b-123">Дополнительные сведения о переходе между состояниями во время репликации представлены [на компьютере с состоянием репликации](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="4538b-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="4538b-124">API репликации</span><span class="sxs-lookup"><span data-stu-id="4538b-124">The Replication API</span></span>

<span data-ttu-id="4538b-125">API репликации предоставляет следующие дефинтионс, типы данных и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4538b-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="4538b-126">Пример реализации поставщика услуг хранения для файлов личных папок с оболочкой (PST) представлен [в примере примера поставщика упакованного PST-хранилища](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4538b-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="4538b-127">Определения</span><span class="sxs-lookup"><span data-stu-id="4538b-127">Definitions:</span></span>
  
- [<span data-ttu-id="4538b-128">Константы для API репликации</span><span class="sxs-lookup"><span data-stu-id="4538b-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="4538b-129">Обязанностей</span><span class="sxs-lookup"><span data-stu-id="4538b-129">Functions:</span></span>
  
- <span data-ttu-id="4538b-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="4538b-131">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="4538b-131">Data types:</span></span>
  
- <span data-ttu-id="4538b-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="4538b-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="4538b-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="4538b-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="4538b-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="4538b-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="4538b-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="4538b-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="4538b-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="4538b-141">**[Синхр](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="4538b-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="4538b-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="4538b-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="4538b-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="4538b-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="4538b-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="4538b-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="4538b-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="4538b-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="4538b-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="4538b-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="4538b-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="4538b-154">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="4538b-154">Interfaces:</span></span>
  
- <span data-ttu-id="4538b-155">**[иосткс](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="4538b-156">**[ипсткс](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="4538b-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="4538b-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="4538b-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="4538b-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="4538b-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="4538b-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

