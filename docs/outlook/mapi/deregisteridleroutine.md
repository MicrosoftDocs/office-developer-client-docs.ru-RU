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
ms.openlocfilehash: 78d499dabe60a8051c6a2a77abad4b7d6f2ed159
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591956"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="95381-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="95381-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="95381-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95381-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95381-105">Удаляет [FNIDLE](fnidle.md) на основе простоя общей процедуры из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="95381-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95381-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="95381-106">Header file:</span></span>  <br/> |<span data-ttu-id="95381-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="95381-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="95381-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="95381-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="95381-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="95381-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="95381-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="95381-110">Called by:</span></span>  <br/> |<span data-ttu-id="95381-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="95381-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="95381-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="95381-112">Parameters</span></span>

 <span data-ttu-id="95381-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="95381-113">_ftg_</span></span>
  
> <span data-ttu-id="95381-114">[in] Функция тег, идентифицирующий простоя процедуры требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="95381-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95381-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95381-115">Return value</span></span>

<span data-ttu-id="95381-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="95381-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95381-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="95381-117">Remarks</span></span>

<span data-ttu-id="95381-118">Любой из задач в клиентском приложении или поставщик услуг можно отменить регистрацию любой простоя подпрограммы, для которого он имеет допустимый _ftg_ параметр.</span><span class="sxs-lookup"><span data-stu-id="95381-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="95381-119">В частности простоя процедуры можно отменить регистрацию самого.</span><span class="sxs-lookup"><span data-stu-id="95381-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="95381-120">Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры:</span><span class="sxs-lookup"><span data-stu-id="95381-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="95381-121">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="95381-121">**Idle routine function**</span></span>|<span data-ttu-id="95381-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="95381-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95381-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="95381-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="95381-124">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="95381-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="95381-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="95381-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="95381-126">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="95381-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="95381-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="95381-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="95381-128">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="95381-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="95381-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="95381-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="95381-130">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="95381-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="95381-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="95381-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="95381-132">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="95381-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="95381-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="95381-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="95381-134">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="95381-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="95381-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="95381-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="95381-136">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="95381-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="95381-137">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="95381-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="95381-138">После простоя подпрограммы отменяется, простоя модуль не вызывает его еще раз.</span><span class="sxs-lookup"><span data-stu-id="95381-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="95381-139">Любой реализации, который вызывает **DeregisterIdleRoutine** необходимо отменить любые блоки памяти, к которым он передается указатели простоя системы в его исходное вызове функции **FtgRegisterIdleRoutine** .</span><span class="sxs-lookup"><span data-stu-id="95381-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

