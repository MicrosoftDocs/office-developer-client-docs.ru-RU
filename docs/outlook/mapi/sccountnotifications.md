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
# <a name="sccountnotifications"></a><span data-ttu-id="102f4-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="102f4-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="102f4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="102f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="102f4-105">Определяет размер массива уведомлений о событиях (в bytes) и проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="102f4-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="102f4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="102f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="102f4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="102f4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="102f4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="102f4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="102f4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="102f4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="102f4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="102f4-110">Called by:</span></span>  <br/> |<span data-ttu-id="102f4-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="102f4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="102f4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="102f4-112">Parameters</span></span>

 <span data-ttu-id="102f4-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="102f4-113">_cntf_</span></span>
  
> <span data-ttu-id="102f4-114">[in] Количество структур [NOTIFICATION](notification.md) в массиве, указанных параметром _rgntf._</span><span class="sxs-lookup"><span data-stu-id="102f4-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="102f4-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="102f4-115">_rgntf_</span></span>
  
> <span data-ttu-id="102f4-116">[in] Указатель на массив структур **УВЕДОМЛЕНий,** размер которых необходимо определить.</span><span class="sxs-lookup"><span data-stu-id="102f4-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="102f4-117">_pcb_</span><span class="sxs-lookup"><span data-stu-id="102f4-117">_pcb_</span></span>
  
> <span data-ttu-id="102f4-118">[out] Необязательный указатель на размер массива,на который указывает параметр  _rgntf_ (в bytes).</span><span class="sxs-lookup"><span data-stu-id="102f4-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="102f4-119">Если nULL, **ScCountNotifications** проверяет массив уведомлений.</span><span class="sxs-lookup"><span data-stu-id="102f4-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="102f4-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="102f4-120">Return value</span></span>

<span data-ttu-id="102f4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="102f4-121">S_OK</span></span>
  
> <span data-ttu-id="102f4-122">Количество было определено успешно.</span><span class="sxs-lookup"><span data-stu-id="102f4-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="102f4-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="102f4-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="102f4-124">Было выявилось недопустимое уведомление.</span><span class="sxs-lookup"><span data-stu-id="102f4-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="102f4-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="102f4-125">Remarks</span></span>

<span data-ttu-id="102f4-126">Если в параметре _PCB_ передается NULL, функция **ScCountNotifications** проверяет только массив уведомлений, но подсчет не делается; Если в _pcb_ передается ненулевое значение, **ScCountNotifications** определяет размер массива и сохраняет пксб _причины._</span><span class="sxs-lookup"><span data-stu-id="102f4-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="102f4-127">Параметр  _pcb_ должен быть достаточно большим, чтобы содержать весь массив.</span><span class="sxs-lookup"><span data-stu-id="102f4-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

