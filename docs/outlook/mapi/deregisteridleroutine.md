---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404563"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="c5c78-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c5c78-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="c5c78-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5c78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5c78-105">Удаляет процедуру бездействия на основе [FNIDLE](fnidle.md) из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5c78-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5c78-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c5c78-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5c78-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c5c78-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c5c78-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c5c78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c5c78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c5c78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c5c78-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c5c78-110">Called by:</span></span>  <br/> |<span data-ttu-id="c5c78-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c5c78-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="c5c78-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5c78-112">Parameters</span></span>

 <span data-ttu-id="c5c78-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="c5c78-113">_ftg_</span></span>
  
> <span data-ttu-id="c5c78-114">[in] Тег функции, определяя процедуру простоя, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="c5c78-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5c78-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5c78-115">Return value</span></span>

<span data-ttu-id="c5c78-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="c5c78-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5c78-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5c78-117">Remarks</span></span>

<span data-ttu-id="c5c78-118">Любая задача в клиентских приложениях или поставщиках служб может отоздать регистрацию любой процедуры бездействия, для которой она имеет допустимый _параметр ftg._</span><span class="sxs-lookup"><span data-stu-id="c5c78-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="c5c78-119">В частности, простаиваемая процедура может отоздать регистрацию.</span><span class="sxs-lookup"><span data-stu-id="c5c78-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="c5c78-120">Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="c5c78-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="c5c78-121">**Простаиваемая подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="c5c78-121">**Idle routine function**</span></span>|<span data-ttu-id="c5c78-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="c5c78-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5c78-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c5c78-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="c5c78-124">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="c5c78-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="c5c78-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="c5c78-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="c5c78-126">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5c78-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="c5c78-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c5c78-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="c5c78-128">Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5c78-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="c5c78-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c5c78-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="c5c78-130">Добавляет процедуру бездействия в систему MAPI с включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="c5c78-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="c5c78-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="c5c78-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="c5c78-132">Выключает механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="c5c78-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="c5c78-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="c5c78-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="c5c78-134">Инициализирует механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="c5c78-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="c5c78-135">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве входного параметра тег функции, возвращенный **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="c5c78-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="c5c78-136">Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="c5c78-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="c5c78-137">Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="c5c78-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="c5c78-138">После того как процедура простоя будет отознана, механизм простоя не будет вызывать ее снова.</span><span class="sxs-lookup"><span data-stu-id="c5c78-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="c5c78-139">Любая реализация, вызываемая **DeregisterIdleRoutine,** должна иметь дело с блоками памяти, в которые он передал указатели, чтобы механизм бездействия использовали его при первоначальном вызове функции **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="c5c78-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

