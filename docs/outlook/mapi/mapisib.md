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
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418710"
---
# <a name="mapisib"></a><span data-ttu-id="35167-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="35167-103">MAPISIB</span></span>

  
  
<span data-ttu-id="35167-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35167-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35167-105">Эта структура используется с [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="35167-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="35167-106">"Участники"</span><span class="sxs-lookup"><span data-stu-id="35167-106">Members</span></span>

 <span data-ttu-id="35167-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="35167-107">**ulSize**</span></span>
  
> <span data-ttu-id="35167-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="35167-108">The size of the structure.</span></span>
    
 <span data-ttu-id="35167-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="35167-109">**ulFlags**</span></span>
  
> <span data-ttu-id="35167-110">Флаг, который указывает тип синхронизации. Это должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="35167-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="35167-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="35167-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="35167-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="35167-112">0x00000200</span></span>  <br/> |<span data-ttu-id="35167-113">Отправка сообщения на сервер (в настоящее время не используется).</span><span class="sxs-lookup"><span data-stu-id="35167-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="35167-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="35167-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="35167-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="35167-115">0x00000001</span></span>  <br/> |<span data-ttu-id="35167-116">Нажмите изменения иерархии на сервер.</span><span class="sxs-lookup"><span data-stu-id="35167-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="35167-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="35167-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="35167-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="35167-118">0x00000002</span></span>  <br/> |<span data-ttu-id="35167-119">Извлеките изменения иерархии с сервера.</span><span class="sxs-lookup"><span data-stu-id="35167-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="35167-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="35167-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="35167-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="35167-121">0x00000040</span></span>  <br/> |<span data-ttu-id="35167-122">Нажмите изменения сообщения на сервер.</span><span class="sxs-lookup"><span data-stu-id="35167-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="35167-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="35167-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="35167-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="35167-124">0x00000080</span></span>  <br/> |<span data-ttu-id="35167-125">Извлеките изменения сообщений с сервера.</span><span class="sxs-lookup"><span data-stu-id="35167-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="35167-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="35167-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="35167-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="35167-127">0x20000000</span></span>  <br/> |<span data-ttu-id="35167-128">Синхронизация была инициирована пользователем и должна быть более приоритетной.</span><span class="sxs-lookup"><span data-stu-id="35167-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="35167-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="35167-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="35167-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="35167-130">0x02000000</span></span>  <br/> |<span data-ttu-id="35167-131">Следует синхронизировать только заготки, а не полные органы.</span><span class="sxs-lookup"><span data-stu-id="35167-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="35167-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="35167-132">**psesSync**</span></span>
  
> <span data-ttu-id="35167-133">[IN] Указатель на сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="35167-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="35167-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="35167-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="35167-135">[IN] Указатель на интерфейс, по которому необходимо обеспечить прогресс.</span><span class="sxs-lookup"><span data-stu-id="35167-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="35167-136">Он может использоваться для запроса интерфейса [для IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="35167-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="35167-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="35167-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="35167-138">[OUT] Событие, которое произойдет, когда только что созданный поток завершится.</span><span class="sxs-lookup"><span data-stu-id="35167-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="35167-139">Указатель должен быть допустимым, так как он будет содержать событие.</span><span class="sxs-lookup"><span data-stu-id="35167-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35167-140">См. также</span><span class="sxs-lookup"><span data-stu-id="35167-140">See also</span></span>



[<span data-ttu-id="35167-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35167-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="35167-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35167-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

