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
# <a name="about-the-replication-api"></a><span data-ttu-id="8b5b3-103">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="8b5b3-103">About the Replication API</span></span>

  
  
<span data-ttu-id="8b5b3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b5b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b5b3-105">API репликации предоставляет поставщику сообщений MAPI функции синхронизации элементов Microsoft Outlook 2013 или Microsoft Outlook 2010, русская версия между сервером и частным локальным магазином на основе PST, созданным для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b5b3-106">Поставщик хранения сообщений MAPI должен реализовать API репликации в соответствии с инструкциями в компьютере состояния [репликации.](about-the-replication-state-machine.md)</span><span class="sxs-lookup"><span data-stu-id="8b5b3-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="8b5b3-107">Поставщик должен использовать API только в личном магазине, созданном для себя, а не в личных магазинах, созданных для других поставщиков, так как личные магазины, созданные для других поставщиков, возможно, уже создали собственные механизмы репликации на соответствующем сервере.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="8b5b3-108">Например, автономный файл папки (.ost) поддерживает собственные отношения репликации с сервером Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="8b5b3-109">Чтобы использовать API репликации, поставщик хранения сообщений MAPI должен сначала открыть и обернуть локальный магазин на основе PST, позвонив **[в NSTServiceEntry.](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="8b5b3-110">Затем поставщик может использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)** для выполнения репликации.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="8b5b3-111">**IPSTX** предоставляется путем запроса в [IMsgStore : IMAPIProp,](imsgstoreimapiprop.md)а **IOSTX** **[предоставляется IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="8b5b3-112">Интерфейс IOSTX</span><span class="sxs-lookup"><span data-stu-id="8b5b3-112">The IOSTX Interface</span></span>

<span data-ttu-id="8b5b3-113">Интерфейс **IOSTX** — это основной интерфейс, который выполняет синхронизацию в API репликации.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="8b5b3-114">**IOSTX** перемещает локальный магазин через ряд штатов, искомую информацию в каждом состоянии об изменениях в локальном магазине, а также информируя локальный магазин об изменениях на сервере.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="8b5b3-115">API репликации также указывает множество структур данных, которые поддерживают синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="8b5b3-116">Поставщик магазина, как клиент этого API, использует API репликации для обертывания локального магазина и перемещения по этим состояниям, нажимая изменения в локальном магазине (например, изменения в иерархии папок или добавление новых элементов) на сервер, а также получения сведений об изменениях на сервере и предоставления этих сведений **интерфейсу IOSTX.**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="8b5b3-117">Интерфейс **IOSTX** принимает инкрементную синхронизацию изменений (ICS), предоставляемую Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="8b5b3-118">Дополнительные сведения о ICS см. в дополнительных сведениях о [критериях оценки ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b5b3-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="8b5b3-119">С **помощью IOSTX** клиент использует ICS для мониторинга и синхронизации дополнительных изменений в иерархии или контенте локального магазина.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="8b5b3-120">Интерфейс IPSTX</span><span class="sxs-lookup"><span data-stu-id="8b5b3-120">The IPSTX Interface</span></span>

 <span data-ttu-id="8b5b3-121">**IPSTX и** пять других интерфейсов \*\*IPSTX *n\*\*,* унаследованных от **IPSTX,** предоставляют дополнительные функции, которые можно использовать при выполнении репликации с помощью интерфейса **IOSTX.**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="8b5b3-122">Например, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** позволяет заставить локальный магазин подражать диспетчеру протоколов Outlook, чтобы перенаправление исходяющих сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="8b5b3-123">Дополнительные сведения о переходах состояния во время репликации см. в дополнительных сведениях о машине состояния [репликации.](about-the-replication-state-machine.md)</span><span class="sxs-lookup"><span data-stu-id="8b5b3-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="8b5b3-124">API репликации</span><span class="sxs-lookup"><span data-stu-id="8b5b3-124">The Replication API</span></span>

<span data-ttu-id="8b5b3-125">API репликации содержит следующие defintions, типы данных и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="8b5b3-126">Пример реализации поставщика магазинов для упакованных файлов личных папок (PST) см. в примере Поставщика упакованных [PST-магазинов.](about-the-sample-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="8b5b3-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="8b5b3-127">Определения</span><span class="sxs-lookup"><span data-stu-id="8b5b3-127">Definitions:</span></span>
  
- [<span data-ttu-id="8b5b3-128">Константы для API репликации</span><span class="sxs-lookup"><span data-stu-id="8b5b3-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="8b5b3-129">Функции:</span><span class="sxs-lookup"><span data-stu-id="8b5b3-129">Functions:</span></span>
  
- <span data-ttu-id="8b5b3-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="8b5b3-131">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="8b5b3-131">Data types:</span></span>
  
- <span data-ttu-id="8b5b3-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="8b5b3-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="8b5b3-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="8b5b3-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="8b5b3-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="8b5b3-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="8b5b3-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="8b5b3-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="8b5b3-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="8b5b3-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="8b5b3-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="8b5b3-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="8b5b3-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="8b5b3-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="8b5b3-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="8b5b3-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="8b5b3-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="8b5b3-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="8b5b3-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="8b5b3-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="8b5b3-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="8b5b3-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="8b5b3-154">Интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="8b5b3-154">Interfaces:</span></span>
  
- <span data-ttu-id="8b5b3-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="8b5b3-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="8b5b3-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="8b5b3-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="8b5b3-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="8b5b3-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="8b5b3-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

