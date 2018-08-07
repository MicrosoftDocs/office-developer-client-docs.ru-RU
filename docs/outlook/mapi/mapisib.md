---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809901"
---
# <a name="mapisib"></a><span data-ttu-id="5b623-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="5b623-103">MAPISIB</span></span>

  
  
<span data-ttu-id="5b623-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b623-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b623-105">Эта структура используется с [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="5b623-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a><span data-ttu-id="5b623-106">Members</span><span class="sxs-lookup"><span data-stu-id="5b623-106">Members</span></span>

 <span data-ttu-id="5b623-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="5b623-107">**ulSize**</span></span>
  
> <span data-ttu-id="5b623-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="5b623-108">The size of the structure.</span></span>
    
 <span data-ttu-id="5b623-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5b623-109">**ulFlags**</span></span>
  
> <span data-ttu-id="5b623-110">Флаг, указывающий тип синхронизации. Оно должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5b623-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="5b623-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="5b623-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="5b623-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="5b623-112">0x00000200</span></span>  <br/> |<span data-ttu-id="5b623-113">Отправьте сообщение на сервер (не в настоящее время).</span><span class="sxs-lookup"><span data-stu-id="5b623-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="5b623-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="5b623-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="5b623-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5b623-115">0x00000001</span></span>  <br/> |<span data-ttu-id="5b623-116">Применить изменения иерархии на сервере.</span><span class="sxs-lookup"><span data-stu-id="5b623-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="5b623-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="5b623-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="5b623-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5b623-118">0x00000002</span></span>  <br/> |<span data-ttu-id="5b623-119">Изменения иерархии по запросу с сервера.</span><span class="sxs-lookup"><span data-stu-id="5b623-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="5b623-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="5b623-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="5b623-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="5b623-121">0x00000040</span></span>  <br/> |<span data-ttu-id="5b623-122">Применить изменения сообщения на сервер.</span><span class="sxs-lookup"><span data-stu-id="5b623-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="5b623-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="5b623-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="5b623-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5b623-124">0x00000080</span></span>  <br/> |<span data-ttu-id="5b623-125">Извлечь изменения сообщений с сервера.</span><span class="sxs-lookup"><span data-stu-id="5b623-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="5b623-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="5b623-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="5b623-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="5b623-127">0x20000000</span></span>  <br/> |<span data-ttu-id="5b623-128">Синхронизация была инициирована пользователем и должен быть более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="5b623-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="5b623-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5b623-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="5b623-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="5b623-130">0x02000000</span></span>  <br/> |<span data-ttu-id="5b623-131">Рекомендуется выполнять синхронизацию только заголовки и текст сообщений не полный.</span><span class="sxs-lookup"><span data-stu-id="5b623-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="5b623-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="5b623-132">**psesSync**</span></span>
  
> <span data-ttu-id="5b623-133">[IN] Указатель на сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="5b623-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="5b623-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="5b623-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="5b623-135">[IN] Указатель на интерфейс для предоставления хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="5b623-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="5b623-136">Его можно использовать для запроса интерфейс для [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="5b623-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="5b623-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="5b623-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="5b623-138">[OUT] Событие, возникающее после завершения потока, который был только что создан.</span><span class="sxs-lookup"><span data-stu-id="5b623-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="5b623-139">Указатель должен быть допустимый, так как он содержит события.</span><span class="sxs-lookup"><span data-stu-id="5b623-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b623-140">См. также</span><span class="sxs-lookup"><span data-stu-id="5b623-140">See also</span></span>



[<span data-ttu-id="5b623-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b623-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="5b623-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b623-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

