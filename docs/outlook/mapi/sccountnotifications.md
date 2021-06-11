---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437996"
---
# <a name="sccountnotifications"></a><span data-ttu-id="3274a-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="3274a-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="3274a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3274a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3274a-105">Определяет размер в bytes массива уведомлений о событиях и проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="3274a-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3274a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3274a-106">Header file:</span></span>  <br/> |<span data-ttu-id="3274a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3274a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3274a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3274a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3274a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3274a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3274a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3274a-110">Called by:</span></span>  <br/> |<span data-ttu-id="3274a-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3274a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="3274a-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="3274a-112">Parameters</span></span>

 <span data-ttu-id="3274a-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="3274a-113">_cntf_</span></span>
  
> <span data-ttu-id="3274a-114">[in] Количество [структур УВЕДОМЛЕНий](notification.md) в массиве, указанных параметром _rgntf._</span><span class="sxs-lookup"><span data-stu-id="3274a-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="3274a-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="3274a-115">_rgntf_</span></span>
  
> <span data-ttu-id="3274a-116">[in] Указатель на массив структур **NOTIFICATION,** размер которых должен быть определен.</span><span class="sxs-lookup"><span data-stu-id="3274a-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="3274a-117">_pcb_</span><span class="sxs-lookup"><span data-stu-id="3274a-117">_pcb_</span></span>
  
> <span data-ttu-id="3274a-118">[вышел] Необязательный указатель на размер в bytes массива, указываемого параметром _rgntf._</span><span class="sxs-lookup"><span data-stu-id="3274a-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="3274a-119">Если NULL, **ScCountNotifications** проверяет массив уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3274a-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3274a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3274a-120">Return value</span></span>

<span data-ttu-id="3274a-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3274a-121">S_OK</span></span>
  
> <span data-ttu-id="3274a-122">Граф был определен успешно.</span><span class="sxs-lookup"><span data-stu-id="3274a-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="3274a-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3274a-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="3274a-124">Недействительное уведомление было встречено.</span><span class="sxs-lookup"><span data-stu-id="3274a-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3274a-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="3274a-125">Remarks</span></span>

<span data-ttu-id="3274a-126">Если NULL передается в _параметре pcb,_ функция **ScCountNotifications** проверяет только массив уведомлений, но подсчет не делается; если значение non-null передается в _pcb,_ **ScCountNotifications** определяет размер массива и сохраняет причину _pcb._</span><span class="sxs-lookup"><span data-stu-id="3274a-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="3274a-127">Параметр  _PCB_ должен быть достаточно большим, чтобы содержать весь массив.</span><span class="sxs-lookup"><span data-stu-id="3274a-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

