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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339398"
---
# <a name="enableidleroutine"></a><span data-ttu-id="c38db-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c38db-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="c38db-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c38db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c38db-105">Включает или отключает подпрограмму бездействия на основе [фнидле](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="c38db-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c38db-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c38db-106">Header file:</span></span>  <br/> |<span data-ttu-id="c38db-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="c38db-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c38db-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c38db-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c38db-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c38db-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c38db-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c38db-110">Called by:</span></span>  <br/> |<span data-ttu-id="c38db-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c38db-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="c38db-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c38db-112">Parameters</span></span>

 <span data-ttu-id="c38db-113">_ФТГ_</span><span class="sxs-lookup"><span data-stu-id="c38db-113">_ftg_</span></span>
  
> <span data-ttu-id="c38db-114">возврата Тег Function, определяющий подпрограмму, подлежащая включению или отключению.</span><span class="sxs-lookup"><span data-stu-id="c38db-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="c38db-115">_Фенабле_</span><span class="sxs-lookup"><span data-stu-id="c38db-115">_fEnable_</span></span>
  
> <span data-ttu-id="c38db-116">возврата Содержит значение TRUE, если антивирусная программа должна включить функцию Idle, или FALSE, если она должна быть отключена.</span><span class="sxs-lookup"><span data-stu-id="c38db-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c38db-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c38db-117">Return value</span></span>

<span data-ttu-id="c38db-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="c38db-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c38db-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c38db-119">Remarks</span></span>

<span data-ttu-id="c38db-120">Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции [фнидле](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="c38db-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="c38db-121">**Функция неАктивности**</span><span class="sxs-lookup"><span data-stu-id="c38db-121">**Idle routine function**</span></span>|<span data-ttu-id="c38db-122">**Usage**</span><span class="sxs-lookup"><span data-stu-id="c38db-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c38db-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c38db-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="c38db-124">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="c38db-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="c38db-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c38db-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="c38db-126">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="c38db-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="c38db-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="c38db-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="c38db-128">Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="c38db-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="c38db-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c38db-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="c38db-130">Добавляет подпрограмму бездействия в систему MAPI с включением или без него.</span><span class="sxs-lookup"><span data-stu-id="c38db-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="c38db-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="c38db-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="c38db-132">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="c38db-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="c38db-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="c38db-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="c38db-134">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="c38db-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="c38db-135">**Чанжеидлераутине**, **дерегистеридлераутине**и **енаблеидлераутине** принимают в качестве входного параметра тег функции, возвращенный методом **фтгрегистеридлераутине**.</span><span class="sxs-lookup"><span data-stu-id="c38db-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="c38db-136">Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="c38db-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="c38db-137">Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="c38db-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

