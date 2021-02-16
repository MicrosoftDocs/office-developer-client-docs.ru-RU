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
# <a name="mapisib"></a><span data-ttu-id="d9b4d-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="d9b4d-103">MAPISIB</span></span>

  
  
<span data-ttu-id="d9b4d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9b4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9b4d-105">Эта структура используется с [IMAPISync::SynchronizeInBackground.](imapisyncsynchronizeinbackground.md)</span><span class="sxs-lookup"><span data-stu-id="d9b4d-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="d9b4d-106">"Участники"</span><span class="sxs-lookup"><span data-stu-id="d9b4d-106">Members</span></span>

 <span data-ttu-id="d9b4d-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="d9b4d-107">**ulSize**</span></span>
  
> <span data-ttu-id="d9b4d-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-108">The size of the structure.</span></span>
    
 <span data-ttu-id="d9b4d-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d9b4d-109">**ulFlags**</span></span>
  
> <span data-ttu-id="d9b4d-110">Флаг, который указывает тип синхронизации. Это должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d9b4d-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="d9b4d-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="d9b4d-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="d9b4d-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="d9b4d-112">0x00000200</span></span>  <br/> |<span data-ttu-id="d9b4d-113">Отправьте сообщение на сервер (в настоящее время не используется).</span><span class="sxs-lookup"><span data-stu-id="d9b4d-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="d9b4d-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="d9b4d-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="d9b4d-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d9b4d-115">0x00000001</span></span>  <br/> |<span data-ttu-id="d9b4d-116">Изменение иерархии push-данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="d9b4d-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="d9b4d-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="d9b4d-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d9b4d-118">0x00000002</span></span>  <br/> |<span data-ttu-id="d9b4d-119">Извлеките изменения иерархии с сервера.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="d9b4d-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="d9b4d-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="d9b4d-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d9b4d-121">0x00000040</span></span>  <br/> |<span data-ttu-id="d9b4d-122">Изменение push-сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="d9b4d-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="d9b4d-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="d9b4d-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d9b4d-124">0x00000080</span></span>  <br/> |<span data-ttu-id="d9b4d-125">Извлеките изменения сообщений с сервера.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="d9b4d-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="d9b4d-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="d9b4d-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="d9b4d-127">0x20000000</span></span>  <br/> |<span data-ttu-id="d9b4d-128">Синхронизация была инициирована пользователем и должна иметь более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="d9b4d-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="d9b4d-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="d9b4d-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="d9b4d-130">0x02000000</span></span>  <br/> |<span data-ttu-id="d9b4d-131">Следует синхронизировать только заглавные и не полные тексты.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="d9b4d-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="d9b4d-132">**psesSync**</span></span>
  
> <span data-ttu-id="d9b4d-133">[IN] Указатель на сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="d9b4d-134">**аcallBack**</span><span class="sxs-lookup"><span data-stu-id="d9b4d-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="d9b4d-135">[IN] Указатель на интерфейс, по которому необходимо обеспечить ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="d9b4d-136">Его можно использовать для запроса интерфейса [для IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d9b4d-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="d9b4d-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="d9b4d-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="d9b4d-138">[OUT] Событие, которое будет происходить после создания только что созданного потока, завершается.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="d9b4d-139">Указатель должен быть действительным, так как он будет содержать событие.</span><span class="sxs-lookup"><span data-stu-id="d9b4d-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9b4d-140">См. также</span><span class="sxs-lookup"><span data-stu-id="d9b4d-140">See also</span></span>



[<span data-ttu-id="d9b4d-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9b4d-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="d9b4d-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9b4d-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

