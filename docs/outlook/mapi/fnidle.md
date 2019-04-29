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
# <a name="fnidle"></a><span data-ttu-id="905bb-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="905bb-103">FNIDLE</span></span>
 
<span data-ttu-id="905bb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="905bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="905bb-105">Определяет процедуру бездействия, которая периодически вызывается модулем бездействия MAPI в соответствии с приоритетом.</span><span class="sxs-lookup"><span data-stu-id="905bb-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="905bb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="905bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="905bb-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="905bb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="905bb-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="905bb-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="905bb-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="905bb-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="905bb-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="905bb-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="905bb-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="905bb-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="905bb-112">Тип соответствующего указателя:</span><span class="sxs-lookup"><span data-stu-id="905bb-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="905bb-113">ПФНИДЛЕ</span><span class="sxs-lookup"><span data-stu-id="905bb-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="905bb-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="905bb-114">Parameters</span></span>

 <span data-ttu-id="905bb-115">_Лпвконтекст_</span><span class="sxs-lookup"><span data-stu-id="905bb-115">_lpvContext_</span></span>
  
> <span data-ttu-id="905bb-116">возврата Указатель на блок памяти, который MAPI передает в подпрограмму бездействия при каждом его вызове.</span><span class="sxs-lookup"><span data-stu-id="905bb-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="905bb-117">Этот указатель передается в модуль бездействия MAPI в параметре _пвидлепарам_ с помощью [фтгрегистеридлераутине](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="905bb-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="905bb-118">Данные в блоке памяти могут предоставлять контекст для вызова в подпрограмму простоя, например, какой объект требуется обработать, или текущее состояние длительной операции.</span><span class="sxs-lookup"><span data-stu-id="905bb-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="905bb-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="905bb-119">Return value</span></span>

<span data-ttu-id="905bb-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="905bb-120">FALSE</span></span> 
  
> <span data-ttu-id="905bb-121">Процедура бездействия с прототипом **фнидле** всегда должна возвращать значение false.</span><span class="sxs-lookup"><span data-stu-id="905bb-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="905bb-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="905bb-122">Remarks</span></span>

<span data-ttu-id="905bb-123">Конкретные функциональные возможности процедуры Idle определяются с помощью реализации клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="905bb-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="905bb-124">Клиент или поставщик должен ограничивать время выполнения каждого состояния неактивной процедуры.</span><span class="sxs-lookup"><span data-stu-id="905bb-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="905bb-125">Каждое состояние должно выполнять минимальный объем обработки, обновлять текущее состояние в контекстных данных, на которые указывает _лпвконтекст_, и возвращать модуль бездействия MAPI.</span><span class="sxs-lookup"><span data-stu-id="905bb-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="905bb-126">Клиент или поставщик должен вызвать функцию MAPI [мапиинитидле](mapiinitidle.md) , прежде чем можно будет зарегистрировать собственную процедуру Idle с помощью вызова функции [фтгрегистеридлераутине](ftgregisteridleroutine.md) .</span><span class="sxs-lookup"><span data-stu-id="905bb-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="905bb-127">Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции ФНИДЛЕ:</span><span class="sxs-lookup"><span data-stu-id="905bb-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="905bb-128">**Функция неАктивности**</span><span class="sxs-lookup"><span data-stu-id="905bb-128">**Idle routine function**</span></span>|<span data-ttu-id="905bb-129">**Usage**</span><span class="sxs-lookup"><span data-stu-id="905bb-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="905bb-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="905bb-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="905bb-131">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="905bb-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="905bb-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="905bb-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="905bb-133">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="905bb-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="905bb-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="905bb-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="905bb-135">Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="905bb-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="905bb-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="905bb-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="905bb-137">Добавляет подпрограмму бездействия в систему MAPI с включением или без него.</span><span class="sxs-lookup"><span data-stu-id="905bb-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="905bb-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="905bb-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="905bb-139">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="905bb-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="905bb-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="905bb-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="905bb-141">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="905bb-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="905bb-142">**Чанжеидлераутине**, **дерегистеридлераутине**и **енаблеидлераутине** принимают в качестве входного параметра тег функции, возвращенный методом **фтгрегистеридлераутине**.</span><span class="sxs-lookup"><span data-stu-id="905bb-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="905bb-143">Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="905bb-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="905bb-144">Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="905bb-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

