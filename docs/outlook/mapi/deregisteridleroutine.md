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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316802"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="65bbe-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="65bbe-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="65bbe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65bbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65bbe-105">Удаляет процедуру бездействия на основе [фнидле](fnidle.md) из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="65bbe-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65bbe-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="65bbe-106">Header file:</span></span>  <br/> |<span data-ttu-id="65bbe-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="65bbe-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="65bbe-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="65bbe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="65bbe-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="65bbe-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="65bbe-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="65bbe-110">Called by:</span></span>  <br/> |<span data-ttu-id="65bbe-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="65bbe-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="65bbe-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="65bbe-112">Parameters</span></span>

 <span data-ttu-id="65bbe-113">_ФТГ_</span><span class="sxs-lookup"><span data-stu-id="65bbe-113">_ftg_</span></span>
  
> <span data-ttu-id="65bbe-114">возврата Тег функции, определяющий подпрограмму, подлежащая удалению.</span><span class="sxs-lookup"><span data-stu-id="65bbe-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65bbe-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65bbe-115">Return value</span></span>

<span data-ttu-id="65bbe-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="65bbe-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65bbe-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="65bbe-117">Remarks</span></span>

<span data-ttu-id="65bbe-118">Любая задача в клиентском приложении или поставщике услуг может отменить регистрацию любой программы, для которой он имеет действительный параметр _ФТГ_ .</span><span class="sxs-lookup"><span data-stu-id="65bbe-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="65bbe-119">В частности, процедура бездействия может отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="65bbe-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="65bbe-120">Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции [фнидле](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="65bbe-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="65bbe-121">**Функция неАктивности**</span><span class="sxs-lookup"><span data-stu-id="65bbe-121">**Idle routine function**</span></span>|<span data-ttu-id="65bbe-122">**Usage**</span><span class="sxs-lookup"><span data-stu-id="65bbe-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65bbe-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="65bbe-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="65bbe-124">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="65bbe-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="65bbe-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="65bbe-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="65bbe-126">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="65bbe-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="65bbe-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="65bbe-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="65bbe-128">Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="65bbe-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="65bbe-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="65bbe-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="65bbe-130">Добавляет подпрограмму бездействия в систему MAPI с включением или без него.</span><span class="sxs-lookup"><span data-stu-id="65bbe-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="65bbe-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="65bbe-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="65bbe-132">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="65bbe-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="65bbe-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="65bbe-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="65bbe-134">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="65bbe-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="65bbe-135">**Чанжеидлераутине**, **дерегистеридлераутине**и **енаблеидлераутине** принимают в качестве входного параметра тег функции, возвращенный методом **фтгрегистеридлераутине**.</span><span class="sxs-lookup"><span data-stu-id="65bbe-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="65bbe-136">Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="65bbe-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="65bbe-137">Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="65bbe-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="65bbe-138">После отмены регистрации неактивной подсистемы не вызывает его повторно.</span><span class="sxs-lookup"><span data-stu-id="65bbe-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="65bbe-139">Любая реализация, вызывающая **дерегистеридлераутине** , должна выделять блоки памяти, в которые она передавала указатели на незанятую подсистему для использования в исходном вызове функции **фтгрегистеридлераутине** .</span><span class="sxs-lookup"><span data-stu-id="65bbe-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

