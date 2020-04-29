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
# <a name="mapiinitidle"></a><span data-ttu-id="319f0-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="319f0-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="319f0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="319f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="319f0-105">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="319f0-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="319f0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="319f0-106">Header file:</span></span>  <br/> |<span data-ttu-id="319f0-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="319f0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="319f0-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="319f0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="319f0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="319f0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="319f0-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="319f0-110">Called by:</span></span>  <br/> |<span data-ttu-id="319f0-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="319f0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="319f0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="319f0-112">Parameters</span></span>

 <span data-ttu-id="319f0-113">_лпвресервед_</span><span class="sxs-lookup"><span data-stu-id="319f0-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="319f0-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="319f0-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="319f0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="319f0-115">Return value</span></span>

<span data-ttu-id="319f0-116">При успешном завершении инициализации функция **мапиинитидле** возвращает ноль, а в противном случае — значение 1.</span><span class="sxs-lookup"><span data-stu-id="319f0-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="319f0-117">Если **мапиинитидле** вызывается несколько раз, все дополнительные вызовы выполняются успешно, но игнорируются, за исключением значения счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="319f0-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="319f0-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="319f0-118">Remarks</span></span>

<span data-ttu-id="319f0-119">Клиентское приложение или поставщик услуг должен вызвать **мапиинитидле** , прежде чем вызывать любую другую функцию модуля бездействия.</span><span class="sxs-lookup"><span data-stu-id="319f0-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="319f0-120">Каждый вызов **мапиинитидле** должен быть сопоставлен последующему вызову [мапидеинитидле](mapideinitidle.md), иначе для вызывающего приложения остается запущен модуль простоя.</span><span class="sxs-lookup"><span data-stu-id="319f0-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="319f0-121">Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции [фнидле](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="319f0-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="319f0-122">**Функция неактивности**</span><span class="sxs-lookup"><span data-stu-id="319f0-122">**Idle routine function**</span></span>|<span data-ttu-id="319f0-123">**Usage**</span><span class="sxs-lookup"><span data-stu-id="319f0-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="319f0-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="319f0-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="319f0-125">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="319f0-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="319f0-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="319f0-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="319f0-127">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="319f0-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="319f0-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="319f0-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="319f0-129">Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="319f0-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="319f0-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="319f0-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="319f0-131">Добавляет подпрограмму бездействия в систему MAPI с включением или без него.</span><span class="sxs-lookup"><span data-stu-id="319f0-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="319f0-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="319f0-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="319f0-133">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="319f0-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="319f0-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="319f0-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="319f0-135">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="319f0-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="319f0-136">Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="319f0-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="319f0-137">Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="319f0-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

