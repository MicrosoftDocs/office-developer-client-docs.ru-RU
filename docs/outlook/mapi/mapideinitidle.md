---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 33f4634623662b7bc09e0830e8bd0b51adc7799d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583500"
---
# <a name="mapideinitidle"></a><span data-ttu-id="08f10-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="08f10-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="08f10-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08f10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08f10-105">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="08f10-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08f10-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="08f10-106">Header file:</span></span>  <br/> |<span data-ttu-id="08f10-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="08f10-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="08f10-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="08f10-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="08f10-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="08f10-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="08f10-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="08f10-110">Called by:</span></span>  <br/> |<span data-ttu-id="08f10-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="08f10-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="08f10-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="08f10-112">Parameters</span></span>

<span data-ttu-id="08f10-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="08f10-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="08f10-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08f10-114">Return value</span></span>

<span data-ttu-id="08f10-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="08f10-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08f10-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="08f10-116">Remarks</span></span>

<span data-ttu-id="08f10-117">Клиентское приложение или поставщик услуг должен вызывать **MAPIDeInitIdle** , когда больше нет необходимости простоя модуля, например, когда он должен остановить обработку.</span><span class="sxs-lookup"><span data-stu-id="08f10-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="08f10-118">Каждый вызов [MAPIInitIdle](mapiinitidle.md) должна совпадать с следующий вызов **MAPIDeInitIdle**или простоя модуль остается для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="08f10-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="08f10-119">Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры:</span><span class="sxs-lookup"><span data-stu-id="08f10-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="08f10-120">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="08f10-120">**Idle routine function**</span></span>|<span data-ttu-id="08f10-121">**Использование**</span><span class="sxs-lookup"><span data-stu-id="08f10-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08f10-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="08f10-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="08f10-123">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="08f10-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="08f10-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="08f10-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="08f10-125">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="08f10-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="08f10-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="08f10-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="08f10-127">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="08f10-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="08f10-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="08f10-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="08f10-129">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="08f10-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="08f10-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="08f10-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="08f10-131">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="08f10-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="08f10-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="08f10-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="08f10-133">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="08f10-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="08f10-134">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="08f10-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="08f10-135">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="08f10-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

