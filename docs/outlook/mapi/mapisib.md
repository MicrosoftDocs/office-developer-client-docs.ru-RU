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
# <a name="mapisib"></a><span data-ttu-id="4788e-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="4788e-103">MAPISIB</span></span>

  
  
<span data-ttu-id="4788e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4788e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4788e-105">Эта структура используется с [имаписинк:: синчронизеинбаккграунд](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="4788e-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="4788e-106">Members</span><span class="sxs-lookup"><span data-stu-id="4788e-106">Members</span></span>

 <span data-ttu-id="4788e-107">**Улсизе**</span><span class="sxs-lookup"><span data-stu-id="4788e-107">**ulSize**</span></span>
  
> <span data-ttu-id="4788e-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="4788e-108">The size of the structure.</span></span>
    
 <span data-ttu-id="4788e-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4788e-109">**ulFlags**</span></span>
  
> <span data-ttu-id="4788e-110">Флаг, указывающий тип синхронизации. Он должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4788e-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="4788e-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="4788e-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="4788e-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="4788e-112">0x00000200</span></span>  <br/> |<span data-ttu-id="4788e-113">Отправьте сообщение на сервер (в данный момент не используется).</span><span class="sxs-lookup"><span data-stu-id="4788e-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="4788e-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="4788e-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="4788e-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4788e-115">0x00000001</span></span>  <br/> |<span data-ttu-id="4788e-116">Принудительная отправка изменений иерархии на сервер.</span><span class="sxs-lookup"><span data-stu-id="4788e-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="4788e-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="4788e-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="4788e-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4788e-118">0x00000002</span></span>  <br/> |<span data-ttu-id="4788e-119">Изменение иерархии по запросу с сервера.</span><span class="sxs-lookup"><span data-stu-id="4788e-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="4788e-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="4788e-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="4788e-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="4788e-121">0x00000040</span></span>  <br/> |<span data-ttu-id="4788e-122">Push-сообщения изменяются на сервер.</span><span class="sxs-lookup"><span data-stu-id="4788e-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="4788e-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="4788e-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="4788e-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="4788e-124">0x00000080</span></span>  <br/> |<span data-ttu-id="4788e-125">Изменение сообщений с сервера.</span><span class="sxs-lookup"><span data-stu-id="4788e-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="4788e-126">СИНК_ОН_ДЕМАНД</span><span class="sxs-lookup"><span data-stu-id="4788e-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="4788e-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="4788e-127">0x20000000</span></span>  <br/> |<span data-ttu-id="4788e-128">Синхронизация была инициирована пользователем и должна иметь более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="4788e-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="4788e-129">СИНК_ГЛОБАЛ_ХЕАДЕРС</span><span class="sxs-lookup"><span data-stu-id="4788e-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="4788e-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="4788e-130">0x02000000</span></span>  <br/> |<span data-ttu-id="4788e-131">Должны синхронизироваться только заголовки и не полные тексты.</span><span class="sxs-lookup"><span data-stu-id="4788e-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="4788e-132">**Псессинк**</span><span class="sxs-lookup"><span data-stu-id="4788e-132">**psesSync**</span></span>
  
> <span data-ttu-id="4788e-133">ВОЗВРАТА Указатель на сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="4788e-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="4788e-134">**Пунккаллбакк**</span><span class="sxs-lookup"><span data-stu-id="4788e-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="4788e-135">ВОЗВРАТА Указатель на интерфейс, для которого необходимо предоставить ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="4788e-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="4788e-136">Его можно использовать для запроса интерфейса для [имаписинкпрогресскаллбакк: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="4788e-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="4788e-137">**\*Фсинкдонивент**</span><span class="sxs-lookup"><span data-stu-id="4788e-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="4788e-138">ВЫШЛИ Событие, которое будет происходить при завершении созданного вами потока.</span><span class="sxs-lookup"><span data-stu-id="4788e-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="4788e-139">Указатель должен быть допустимым, так как он будет содержать событие.</span><span class="sxs-lookup"><span data-stu-id="4788e-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4788e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4788e-140">See also</span></span>



[<span data-ttu-id="4788e-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4788e-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="4788e-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4788e-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

