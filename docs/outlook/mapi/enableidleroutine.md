---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c53bd63e60281e999d0d379913b3609e9472a40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579279"
---
# <a name="enableidleroutine"></a><span data-ttu-id="5fa8d-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5fa8d-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="5fa8d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fa8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fa8d-105">Включает или отключает простаивающее подпрограмма [FNIDLE](fnidle.md) на основе.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fa8d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5fa8d-106">Header file:</span></span>  <br/> |<span data-ttu-id="5fa8d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5fa8d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5fa8d-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="5fa8d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5fa8d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5fa8d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5fa8d-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="5fa8d-110">Called by:</span></span>  <br/> |<span data-ttu-id="5fa8d-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="5fa8d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="5fa8d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fa8d-112">Parameters</span></span>

 <span data-ttu-id="5fa8d-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="5fa8d-113">_ftg_</span></span>
  
> <span data-ttu-id="5fa8d-114">[in] Функция тег, идентифицирующий простоя процедуру для включения или выключения.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="5fa8d-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="5fa8d-115">_fEnable_</span></span>
  
> <span data-ttu-id="5fa8d-116">[in] Содержит значение TRUE, если простоя модуль следует включите простоя подпрограммы, или значение FALSE, если его следует отключить.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5fa8d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fa8d-117">Return value</span></span>

<span data-ttu-id="5fa8d-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fa8d-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="5fa8d-119">Remarks</span></span>

<span data-ttu-id="5fa8d-120">Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры:</span><span class="sxs-lookup"><span data-stu-id="5fa8d-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="5fa8d-121">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="5fa8d-121">**Idle routine function**</span></span>|<span data-ttu-id="5fa8d-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="5fa8d-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fa8d-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5fa8d-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="5fa8d-124">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="5fa8d-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5fa8d-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="5fa8d-126">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="5fa8d-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="5fa8d-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="5fa8d-128">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5fa8d-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5fa8d-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="5fa8d-130">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="5fa8d-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="5fa8d-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="5fa8d-132">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="5fa8d-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="5fa8d-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="5fa8d-134">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="5fa8d-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="5fa8d-136">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="5fa8d-137">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

