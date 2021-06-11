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
# <a name="deregisteridleroutine"></a><span data-ttu-id="b7de2-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b7de2-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="b7de2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7de2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7de2-105">Удаляет режим простоя на основе [FNIDLE](fnidle.md) из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7de2-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7de2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b7de2-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7de2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b7de2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b7de2-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b7de2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7de2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b7de2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b7de2-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b7de2-110">Called by:</span></span>  <br/> |<span data-ttu-id="b7de2-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b7de2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="b7de2-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b7de2-112">Parameters</span></span>

 <span data-ttu-id="b7de2-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="b7de2-113">_ftg_</span></span>
  
> <span data-ttu-id="b7de2-114">[in] Тег function, который определяет режим простоя, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="b7de2-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7de2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7de2-115">Return value</span></span>

<span data-ttu-id="b7de2-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="b7de2-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7de2-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7de2-117">Remarks</span></span>

<span data-ttu-id="b7de2-118">Любая задача в клиентских приложениях или поставщике услуг может отстранить любую праздную процедуру, для которой она имеет допустимый _параметр ftg._</span><span class="sxs-lookup"><span data-stu-id="b7de2-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="b7de2-119">В частности, простаивающим режимом может быть само зарегистриро-</span><span class="sxs-lookup"><span data-stu-id="b7de2-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="b7de2-120">Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="b7de2-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="b7de2-121">**Простаиваемая рутинная функция**</span><span class="sxs-lookup"><span data-stu-id="b7de2-121">**Idle routine function**</span></span>|<span data-ttu-id="b7de2-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="b7de2-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7de2-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b7de2-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="b7de2-124">Изменяет характеристики зарегистрированного режима простоя.</span><span class="sxs-lookup"><span data-stu-id="b7de2-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="b7de2-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="b7de2-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="b7de2-126">Удаляет зарегистрированную процедуру простоя из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7de2-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="b7de2-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b7de2-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="b7de2-128">Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7de2-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="b7de2-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b7de2-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="b7de2-130">Добавляет праздную рутину в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="b7de2-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="b7de2-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="b7de2-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="b7de2-132">Отключит простой движок MAPI для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="b7de2-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="b7de2-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="b7de2-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="b7de2-134">Инициализирует простой двигатель MAPI для вызываемой заявки.</span><span class="sxs-lookup"><span data-stu-id="b7de2-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="b7de2-135">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве параметра ввода тег функции, возвращенный **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="b7de2-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="b7de2-136">Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению.</span><span class="sxs-lookup"><span data-stu-id="b7de2-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="b7de2-137">Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета.</span><span class="sxs-lookup"><span data-stu-id="b7de2-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="b7de2-138">После того, как режим простоя будет отозвался, простой двигатель не будет вызывать его снова.</span><span class="sxs-lookup"><span data-stu-id="b7de2-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="b7de2-139">Любая реализация, вызываемая **DeregisterIdleRoutine,** должна иметь дело с любыми блоками памяти, к которым он передал указатели для простоя двигателя для использования в первоначальном вызове функции **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="b7de2-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

