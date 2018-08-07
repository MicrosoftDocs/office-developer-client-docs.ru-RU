---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808470"
---
# <a name="fnidle"></a><span data-ttu-id="4da3c-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="4da3c-103">FNIDLE</span></span>
 
<span data-ttu-id="4da3c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4da3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4da3c-105">Определяет простоя процедуры, которая простоя подсистемы MAPI периодически вызывает в соответствии с приоритетом.</span><span class="sxs-lookup"><span data-stu-id="4da3c-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4da3c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4da3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="4da3c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4da3c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4da3c-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="4da3c-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4da3c-109">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="4da3c-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="4da3c-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="4da3c-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4da3c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4da3c-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="4da3c-112">Соответствующий тип указателя:</span><span class="sxs-lookup"><span data-stu-id="4da3c-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="4da3c-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="4da3c-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="4da3c-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="4da3c-114">Parameters</span></span>

 <span data-ttu-id="4da3c-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="4da3c-115">_lpvContext_</span></span>
  
> <span data-ttu-id="4da3c-116">[in] Указатель на блок памяти, что MAPI передается простоя подпрограммы каждый раз вызывает его.</span><span class="sxs-lookup"><span data-stu-id="4da3c-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="4da3c-117">Такой указатель передается к ядру простоя MAPI с помощью параметра _pvIdleParam_ с [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="4da3c-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="4da3c-118">Данные в блоке памяти может предоставить контекст для вызова простоя действия, например, какие объекта, или текущее состояние длительной операции.</span><span class="sxs-lookup"><span data-stu-id="4da3c-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4da3c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="4da3c-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="4da3c-120">FALSE</span></span> 
  
> <span data-ttu-id="4da3c-121">Простоя процедуру с прототип **FNIDLE** всегда должен возвращать значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="4da3c-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4da3c-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="4da3c-122">Remarks</span></span>

<span data-ttu-id="4da3c-123">Определенных функций простоя подпрограммы определяется при помощи клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="4da3c-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="4da3c-124">Клиента или поставщика необходимо ограничить время выполнения каждого состояния простоя подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="4da3c-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="4da3c-125">Каждого состояния следует выполнить минимальный объем обработки, обновить текущее состояние в данные контекста, который указывает _lpvContext_и вернуться к ядру простоя MAPI.</span><span class="sxs-lookup"><span data-stu-id="4da3c-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="4da3c-126">Клиента или поставщика необходимо вызвать функцию MAPI [MAPIInitIdle](mapiinitidle.md) перед его можно регистрировать свой собственный простоя подпрограммы с вызова функции [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) .</span><span class="sxs-lookup"><span data-stu-id="4da3c-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="4da3c-127">Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции FNIDLE простоя процедуры:</span><span class="sxs-lookup"><span data-stu-id="4da3c-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="4da3c-128">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="4da3c-128">**Idle routine function**</span></span>|<span data-ttu-id="4da3c-129">**Использование**</span><span class="sxs-lookup"><span data-stu-id="4da3c-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4da3c-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4da3c-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="4da3c-131">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="4da3c-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="4da3c-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4da3c-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="4da3c-133">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="4da3c-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="4da3c-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4da3c-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="4da3c-135">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="4da3c-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="4da3c-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4da3c-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="4da3c-137">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="4da3c-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="4da3c-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="4da3c-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="4da3c-139">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="4da3c-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="4da3c-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="4da3c-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="4da3c-141">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="4da3c-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="4da3c-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="4da3c-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="4da3c-143">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="4da3c-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="4da3c-144">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="4da3c-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

