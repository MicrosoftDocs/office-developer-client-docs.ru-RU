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
# <a name="enableidleroutine"></a><span data-ttu-id="54804-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54804-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="54804-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54804-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54804-105">Включает или отключает режим простоя на основе [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="54804-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54804-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="54804-106">Header file:</span></span>  <br/> |<span data-ttu-id="54804-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="54804-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="54804-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="54804-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="54804-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="54804-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="54804-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="54804-110">Called by:</span></span>  <br/> |<span data-ttu-id="54804-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="54804-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="54804-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="54804-112">Parameters</span></span>

 <span data-ttu-id="54804-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="54804-113">_ftg_</span></span>
  
> <span data-ttu-id="54804-114">[in] Тег function, который определяет режим простоя, который необходимо включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="54804-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="54804-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="54804-115">_fEnable_</span></span>
  
> <span data-ttu-id="54804-116">[in] Содержит TRUE, если простой двигатель должен включить режим простоя, или FALSE, если он должен отключить его.</span><span class="sxs-lookup"><span data-stu-id="54804-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54804-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54804-117">Return value</span></span>

<span data-ttu-id="54804-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="54804-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54804-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="54804-119">Remarks</span></span>

<span data-ttu-id="54804-120">Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="54804-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="54804-121">**Простаиваемая рутинная функция**</span><span class="sxs-lookup"><span data-stu-id="54804-121">**Idle routine function**</span></span>|<span data-ttu-id="54804-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="54804-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54804-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54804-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="54804-124">Изменяет характеристики зарегистрированного режима простоя.</span><span class="sxs-lookup"><span data-stu-id="54804-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="54804-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54804-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="54804-126">Удаляет зарегистрированную процедуру простоя из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="54804-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="54804-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="54804-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="54804-128">Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="54804-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="54804-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54804-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="54804-130">Добавляет праздную рутину в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="54804-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="54804-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="54804-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="54804-132">Отключит простой движок MAPI для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="54804-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="54804-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="54804-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="54804-134">Инициализирует простой двигатель MAPI для вызываемой заявки.</span><span class="sxs-lookup"><span data-stu-id="54804-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="54804-135">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве параметра ввода тег функции, возвращенный **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="54804-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="54804-136">Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению.</span><span class="sxs-lookup"><span data-stu-id="54804-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="54804-137">Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета.</span><span class="sxs-lookup"><span data-stu-id="54804-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

