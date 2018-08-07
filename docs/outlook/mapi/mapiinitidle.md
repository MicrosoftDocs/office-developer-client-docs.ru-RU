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
ms.openlocfilehash: e4f4cdd1d0ed2e03d49f471e6e91464b7973c920
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809878"
---
# <a name="mapiinitidle"></a><span data-ttu-id="1acbb-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="1acbb-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="1acbb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1acbb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1acbb-105">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="1acbb-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1acbb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1acbb-106">Header file:</span></span>  <br/> |<span data-ttu-id="1acbb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1acbb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1acbb-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="1acbb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1acbb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1acbb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1acbb-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="1acbb-110">Called by:</span></span>  <br/> |<span data-ttu-id="1acbb-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="1acbb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="1acbb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1acbb-112">Parameters</span></span>

 <span data-ttu-id="1acbb-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="1acbb-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="1acbb-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="1acbb-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1acbb-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1acbb-115">Return value</span></span>

<span data-ttu-id="1acbb-116">Функция **MAPIInitIdle** возвращает ноль при инициализации успешные и 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1acbb-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="1acbb-117">Если **MAPIInitIdle** вызван несколько раз, все дополнительные звонки выполняются успешно, но игнорируется за исключением чтобы увеличивают счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="1acbb-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1acbb-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="1acbb-118">Remarks</span></span>

<span data-ttu-id="1acbb-119">Клиентское приложение или поставщик услуг необходимо вызвать **MAPIInitIdle** перед вызовом других функции простоя модуль.</span><span class="sxs-lookup"><span data-stu-id="1acbb-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="1acbb-120">Каждый вызов **MAPIInitIdle** должна совпадать с следующий вызов [MAPIDeInitIdle](mapideinitidle.md)или простоя модуль остается для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="1acbb-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="1acbb-121">Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры:</span><span class="sxs-lookup"><span data-stu-id="1acbb-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="1acbb-122">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="1acbb-122">**Idle routine function**</span></span>|<span data-ttu-id="1acbb-123">**Использование**</span><span class="sxs-lookup"><span data-stu-id="1acbb-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1acbb-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1acbb-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="1acbb-125">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="1acbb-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="1acbb-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1acbb-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="1acbb-127">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="1acbb-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="1acbb-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1acbb-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="1acbb-129">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="1acbb-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="1acbb-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1acbb-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="1acbb-131">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="1acbb-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="1acbb-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="1acbb-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="1acbb-133">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="1acbb-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="1acbb-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="1acbb-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="1acbb-135">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="1acbb-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="1acbb-136">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="1acbb-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="1acbb-137">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="1acbb-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

