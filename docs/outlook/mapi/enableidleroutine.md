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
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410223"
---
# <a name="enableidleroutine"></a><span data-ttu-id="b3dd0-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b3dd0-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="b3dd0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3dd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3dd0-105">Включает или отключает процедуру бездействия на основе [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="b3dd0-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3dd0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b3dd0-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3dd0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b3dd0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b3dd0-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b3dd0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b3dd0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b3dd0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b3dd0-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b3dd0-110">Called by:</span></span>  <br/> |<span data-ttu-id="b3dd0-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b3dd0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="b3dd0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3dd0-112">Parameters</span></span>

 <span data-ttu-id="b3dd0-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="b3dd0-113">_ftg_</span></span>
  
> <span data-ttu-id="b3dd0-114">[in] Тег функции, определяя процедуру простоя, которую необходимо включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="b3dd0-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="b3dd0-115">_fEnable_</span></span>
  
> <span data-ttu-id="b3dd0-116">[in] Содержит true, если механизм бездействия должен включить процедуру простоя, или FALSE, если он должен отключить его.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b3dd0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3dd0-117">Return value</span></span>

<span data-ttu-id="b3dd0-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3dd0-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3dd0-119">Remarks</span></span>

<span data-ttu-id="b3dd0-120">Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="b3dd0-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="b3dd0-121">**Простаиваемая подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="b3dd0-121">**Idle routine function**</span></span>|<span data-ttu-id="b3dd0-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="b3dd0-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3dd0-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b3dd0-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="b3dd0-124">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="b3dd0-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b3dd0-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="b3dd0-126">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="b3dd0-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="b3dd0-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="b3dd0-128">Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="b3dd0-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b3dd0-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="b3dd0-130">Добавляет процедуру бездействия в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="b3dd0-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="b3dd0-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="b3dd0-132">Выключает механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="b3dd0-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="b3dd0-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="b3dd0-134">Инициализирует механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="b3dd0-135">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве входного параметра тег функции, возвращенный **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="b3dd0-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="b3dd0-136">Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="b3dd0-137">Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

