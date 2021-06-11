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
# <a name="mapiinitidle"></a><span data-ttu-id="a1cf9-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="a1cf9-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="a1cf9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1cf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1cf9-105">Инициализирует простой двигатель MAPI для вызываемой заявки.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1cf9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a1cf9-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1cf9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a1cf9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a1cf9-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a1cf9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1cf9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1cf9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a1cf9-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a1cf9-110">Called by:</span></span>  <br/> |<span data-ttu-id="a1cf9-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a1cf9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="a1cf9-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a1cf9-112">Parameters</span></span>

 <span data-ttu-id="a1cf9-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="a1cf9-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="a1cf9-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1cf9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1cf9-115">Return value</span></span>

<span data-ttu-id="a1cf9-116">Функция **MAPIInitIdle** возвращает ноль при успешной инициализации и 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="a1cf9-117">Если **MAPIInitIdle** вызывается несколько раз, все дополнительные вызовы успешно, но игнорируются, за исключением прибавления отсчета ссылок.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1cf9-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1cf9-118">Remarks</span></span>

<span data-ttu-id="a1cf9-119">Клиентские приложения или поставщик услуг должны вызвать **MAPIInitIdle** перед вызовом любой другой функции простоя двигателя.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="a1cf9-120">Каждый звонок **в MAPIInitIdle** должен соответствовать последующему вызову [MAPIDeInitIdle,](mapideinitidle.md)иначе для вызываемого приложения остается запущен простой двигатель.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="a1cf9-121">Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="a1cf9-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="a1cf9-122">**Простаиваемая рутинная функция**</span><span class="sxs-lookup"><span data-stu-id="a1cf9-122">**Idle routine function**</span></span>|<span data-ttu-id="a1cf9-123">**Использование**</span><span class="sxs-lookup"><span data-stu-id="a1cf9-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1cf9-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a1cf9-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="a1cf9-125">Изменяет характеристики зарегистрированного режима простоя.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="a1cf9-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a1cf9-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="a1cf9-127">Удаляет зарегистрированную процедуру простоя из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="a1cf9-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a1cf9-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="a1cf9-129">Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="a1cf9-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a1cf9-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="a1cf9-131">Добавляет праздную рутину в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="a1cf9-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="a1cf9-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="a1cf9-133">Отключит простой движок MAPI для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="a1cf9-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="a1cf9-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="a1cf9-135">Инициализирует простой двигатель MAPI для вызываемой заявки.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="a1cf9-136">Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="a1cf9-137">Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета.</span><span class="sxs-lookup"><span data-stu-id="a1cf9-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

