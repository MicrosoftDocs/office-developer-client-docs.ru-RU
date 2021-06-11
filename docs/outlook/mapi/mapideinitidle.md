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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408210"
---
# <a name="mapideinitidle"></a><span data-ttu-id="1a4fb-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="1a4fb-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="1a4fb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a4fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a4fb-105">Отключит простой движок MAPI для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a4fb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1a4fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a4fb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1a4fb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1a4fb-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1a4fb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a4fb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1a4fb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1a4fb-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1a4fb-110">Called by:</span></span>  <br/> |<span data-ttu-id="1a4fb-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="1a4fb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="1a4fb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a4fb-112">Parameters</span></span>

<span data-ttu-id="1a4fb-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="1a4fb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a4fb-114">Return value</span></span>

<span data-ttu-id="1a4fb-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a4fb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a4fb-116">Remarks</span></span>

<span data-ttu-id="1a4fb-117">Клиентские приложения или поставщик услуг должны вызывать **MAPIDeInitIdle,** если он больше не нуждается в простое двигателя, например, когда он вот-вот прекратит обработку.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="1a4fb-118">Каждый звонок [в MAPIInitIdle](mapiinitidle.md) должен соответствовать последующему вызову **MAPIDeInitIdle,** иначе для вызываемого приложения остается запущен простой двигатель.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="1a4fb-119">Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа [функции FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="1a4fb-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="1a4fb-120">**Простаиваемая рутинная функция**</span><span class="sxs-lookup"><span data-stu-id="1a4fb-120">**Idle routine function**</span></span>|<span data-ttu-id="1a4fb-121">**Использование**</span><span class="sxs-lookup"><span data-stu-id="1a4fb-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a4fb-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1a4fb-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="1a4fb-123">Изменяет характеристики зарегистрированного режима простоя.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="1a4fb-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1a4fb-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="1a4fb-125">Удаляет зарегистрированную процедуру простоя из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="1a4fb-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1a4fb-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="1a4fb-127">Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="1a4fb-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="1a4fb-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="1a4fb-129">Добавляет праздную рутину в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="1a4fb-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="1a4fb-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="1a4fb-131">Отключит простой движок MAPI для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="1a4fb-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="1a4fb-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="1a4fb-133">Инициализирует простой двигатель MAPI для вызываемой заявки.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="1a4fb-134">Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="1a4fb-135">Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета.</span><span class="sxs-lookup"><span data-stu-id="1a4fb-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

