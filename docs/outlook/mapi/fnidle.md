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
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412382"
---
# <a name="fnidle"></a><span data-ttu-id="9e53d-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="9e53d-103">FNIDLE</span></span>
 
<span data-ttu-id="9e53d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e53d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e53d-105">Определяет режим простоя, который периодически вызывает холостый двигатель MAPI в соответствии с приоритетом.</span><span class="sxs-lookup"><span data-stu-id="9e53d-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e53d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9e53d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e53d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9e53d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9e53d-108">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="9e53d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="9e53d-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9e53d-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="9e53d-110">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="9e53d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="9e53d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="9e53d-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="9e53d-112">Соответствующий тип указателя:</span><span class="sxs-lookup"><span data-stu-id="9e53d-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="9e53d-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="9e53d-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="9e53d-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="9e53d-114">Parameters</span></span>

 <span data-ttu-id="9e53d-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="9e53d-115">_lpvContext_</span></span>
  
> <span data-ttu-id="9e53d-116">[in] Указатель на блок памяти, который MAPI передает в режим простоя при каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="9e53d-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="9e53d-117">Этот указатель передается в простой двигатель MAPI в _параметре pvIdleParam_ [ftgRegisterIdleRoutine.](ftgregisteridleroutine.md)</span><span class="sxs-lookup"><span data-stu-id="9e53d-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="9e53d-118">Данные в блоке памяти могут обеспечить контекст для вызова к режиму простоя, например к объекту, на котором необходимо работать, или текущему состоянии длительной операции.</span><span class="sxs-lookup"><span data-stu-id="9e53d-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e53d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e53d-119">Return value</span></span>

<span data-ttu-id="9e53d-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="9e53d-120">FALSE</span></span> 
  
> <span data-ttu-id="9e53d-121">Простаиваемая процедура с прототипом **FNIDLE** всегда должна возвращать FALSE.</span><span class="sxs-lookup"><span data-stu-id="9e53d-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e53d-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e53d-122">Remarks</span></span>

<span data-ttu-id="9e53d-123">Конкретные функции обычного простоя определяются реализующим клиентом или поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="9e53d-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="9e53d-124">Клиент или поставщик должны ограничить время выполнения каждого состояния обычного простоя.</span><span class="sxs-lookup"><span data-stu-id="9e53d-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="9e53d-125">Каждое состояние должно выполнять минимальный объем обработки, обновлять текущее состояние в контекстных данных, на которые указывает  _lpvContext,_ и возвращаться в простой двигатель MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e53d-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="9e53d-126">Клиент или поставщик должны вызвать функцию [MAPI MAPIInitIdle,](mapiinitidle.md) прежде чем он сможет зарегистрировать свою собственную процедуру простоя с вызовом на функцию [FtgRegisterIdleRoutine.](ftgregisteridleroutine.md)</span><span class="sxs-lookup"><span data-stu-id="9e53d-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="9e53d-127">Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа функции FNIDLE:</span><span class="sxs-lookup"><span data-stu-id="9e53d-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="9e53d-128">**Простаиваемая рутинная функция**</span><span class="sxs-lookup"><span data-stu-id="9e53d-128">**Idle routine function**</span></span>|<span data-ttu-id="9e53d-129">**Использование**</span><span class="sxs-lookup"><span data-stu-id="9e53d-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e53d-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9e53d-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="9e53d-131">Изменяет характеристики зарегистрированного режима простоя.</span><span class="sxs-lookup"><span data-stu-id="9e53d-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="9e53d-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9e53d-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="9e53d-133">Удаляет зарегистрированную процедуру простоя из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e53d-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="9e53d-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9e53d-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="9e53d-135">Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e53d-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="9e53d-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9e53d-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="9e53d-137">Добавляет праздную рутину в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="9e53d-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="9e53d-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="9e53d-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="9e53d-139">Отключит простой движок MAPI для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="9e53d-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="9e53d-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="9e53d-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="9e53d-141">Инициализирует простой двигатель MAPI для вызываемой заявки.</span><span class="sxs-lookup"><span data-stu-id="9e53d-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="9e53d-142">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве параметра ввода тег функции, возвращенный **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="9e53d-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="9e53d-143">Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению.</span><span class="sxs-lookup"><span data-stu-id="9e53d-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="9e53d-144">Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета.</span><span class="sxs-lookup"><span data-stu-id="9e53d-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

