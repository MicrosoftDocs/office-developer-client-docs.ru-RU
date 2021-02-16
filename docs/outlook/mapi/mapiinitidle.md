---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432445"
---
# <a name="mapiinitidle"></a><span data-ttu-id="694b7-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="694b7-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="694b7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="694b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="694b7-105">Инициализирует механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="694b7-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="694b7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="694b7-106">Header file:</span></span>  <br/> |<span data-ttu-id="694b7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="694b7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="694b7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="694b7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="694b7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="694b7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="694b7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="694b7-110">Called by:</span></span>  <br/> |<span data-ttu-id="694b7-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="694b7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="694b7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="694b7-112">Parameters</span></span>

 <span data-ttu-id="694b7-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="694b7-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="694b7-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="694b7-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="694b7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="694b7-115">Return value</span></span>

<span data-ttu-id="694b7-116">Функция **MAPIInitIdle** возвращает ноль при успешной инициализации, а 1 — в противном случае.</span><span class="sxs-lookup"><span data-stu-id="694b7-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="694b7-117">Если **MAPIInitIdle** вызывается несколько раз, все дополнительные вызовы будут успешными, но будут игнорироваться, за исключением того, что добавит количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="694b7-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="694b7-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="694b7-118">Remarks</span></span>

<span data-ttu-id="694b7-119">Клиентские приложения или поставщик службы должны вызвать **MAPIInitIdle перед** вызовом любой другой функции бездействия ядер.</span><span class="sxs-lookup"><span data-stu-id="694b7-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="694b7-120">Каждый вызов **MAPIInitIdle** должен соответствовать последующим вызовом [MAPIDeInitIdle,](mapideinitidle.md)иначе механизм бездействия остается запущенным для вызываемого приложения.</span><span class="sxs-lookup"><span data-stu-id="694b7-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="694b7-121">Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="694b7-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="694b7-122">**Простаиваемая подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="694b7-122">**Idle routine function**</span></span>|<span data-ttu-id="694b7-123">**Использование**</span><span class="sxs-lookup"><span data-stu-id="694b7-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="694b7-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="694b7-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="694b7-125">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="694b7-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="694b7-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="694b7-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="694b7-127">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="694b7-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="694b7-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="694b7-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="694b7-129">Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="694b7-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="694b7-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="694b7-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="694b7-131">Добавляет процедуру бездействия в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="694b7-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="694b7-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="694b7-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="694b7-133">Выключает механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="694b7-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="694b7-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="694b7-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="694b7-135">Инициализирует механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="694b7-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="694b7-136">Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="694b7-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="694b7-137">Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="694b7-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

