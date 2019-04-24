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
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357325"
---
# <a name="mapideinitidle"></a><span data-ttu-id="064f6-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="064f6-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="064f6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="064f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="064f6-105">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="064f6-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="064f6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="064f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="064f6-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="064f6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="064f6-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="064f6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="064f6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="064f6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="064f6-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="064f6-110">Called by:</span></span>  <br/> |<span data-ttu-id="064f6-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="064f6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="064f6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="064f6-112">Parameters</span></span>

<span data-ttu-id="064f6-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="064f6-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="064f6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="064f6-114">Return value</span></span>

<span data-ttu-id="064f6-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="064f6-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="064f6-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="064f6-116">Remarks</span></span>

<span data-ttu-id="064f6-117">Клиентское приложение или поставщик услуг должен вызывать **мапидеинитидле** , когда больше не требуется модуль для бездействия, например, когда он собирается остановить обработку.</span><span class="sxs-lookup"><span data-stu-id="064f6-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="064f6-118">Каждый вызов [мапиинитидле](mapiinitidle.md) должен быть сопоставлен последующему вызову **мапидеинитидле**, иначе для вызывающего приложения остается запущен модуль простоя.</span><span class="sxs-lookup"><span data-stu-id="064f6-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="064f6-119">Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции [фнидле](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="064f6-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="064f6-120">**Функция неАктивности**</span><span class="sxs-lookup"><span data-stu-id="064f6-120">**Idle routine function**</span></span>|<span data-ttu-id="064f6-121">**Usage**</span><span class="sxs-lookup"><span data-stu-id="064f6-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="064f6-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="064f6-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="064f6-123">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="064f6-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="064f6-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="064f6-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="064f6-125">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="064f6-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="064f6-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="064f6-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="064f6-127">Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="064f6-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="064f6-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="064f6-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="064f6-129">Добавляет подпрограмму бездействия в систему MAPI с включением или без него.</span><span class="sxs-lookup"><span data-stu-id="064f6-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="064f6-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="064f6-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="064f6-131">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="064f6-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="064f6-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="064f6-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="064f6-133">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="064f6-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="064f6-134">Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="064f6-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="064f6-135">Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="064f6-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

