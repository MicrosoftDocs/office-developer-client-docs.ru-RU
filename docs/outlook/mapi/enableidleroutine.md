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
ms.openlocfilehash: 00b5c123e588636654fb4287cc7b45500d47d89c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808378"
---
# <a name="enableidleroutine"></a><span data-ttu-id="949b2-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="949b2-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="949b2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="949b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="949b2-105">Включает или отключает простаивающее подпрограмма [FNIDLE](fnidle.md) на основе.</span><span class="sxs-lookup"><span data-stu-id="949b2-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="949b2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="949b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="949b2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="949b2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="949b2-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="949b2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="949b2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="949b2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="949b2-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="949b2-110">Called by:</span></span>  <br/> |<span data-ttu-id="949b2-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="949b2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="949b2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="949b2-112">Parameters</span></span>

 <span data-ttu-id="949b2-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="949b2-113">_ftg_</span></span>
  
> <span data-ttu-id="949b2-114">[in] Функция тег, идентифицирующий простоя процедуру для включения или выключения.</span><span class="sxs-lookup"><span data-stu-id="949b2-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="949b2-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="949b2-115">_fEnable_</span></span>
  
> <span data-ttu-id="949b2-116">[in] Содержит значение TRUE, если простоя модуль следует включите простоя подпрограммы, или значение FALSE, если его следует отключить.</span><span class="sxs-lookup"><span data-stu-id="949b2-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="949b2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="949b2-117">Return value</span></span>

<span data-ttu-id="949b2-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="949b2-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="949b2-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="949b2-119">Remarks</span></span>

<span data-ttu-id="949b2-120">Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры:</span><span class="sxs-lookup"><span data-stu-id="949b2-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="949b2-121">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="949b2-121">**Idle routine function**</span></span>|<span data-ttu-id="949b2-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="949b2-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="949b2-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="949b2-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="949b2-124">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="949b2-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="949b2-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="949b2-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="949b2-126">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="949b2-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="949b2-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="949b2-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="949b2-128">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="949b2-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="949b2-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="949b2-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="949b2-130">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="949b2-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="949b2-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="949b2-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="949b2-132">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="949b2-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="949b2-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="949b2-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="949b2-134">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="949b2-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="949b2-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="949b2-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="949b2-136">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="949b2-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="949b2-137">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="949b2-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

