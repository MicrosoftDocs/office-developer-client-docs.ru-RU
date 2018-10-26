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
ms.openlocfilehash: 923864c625cb032c3b351bb999ff7cc782eae588
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567169"
---
# <a name="sccountnotifications"></a><span data-ttu-id="11f9c-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="11f9c-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="11f9c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11f9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11f9c-105">Определяет размер, в байтах, массива уведомления о событиях и проверки памяти, связанной с массивом.</span><span class="sxs-lookup"><span data-stu-id="11f9c-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11f9c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="11f9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="11f9c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="11f9c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="11f9c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="11f9c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11f9c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="11f9c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="11f9c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="11f9c-110">Called by:</span></span>  <br/> |<span data-ttu-id="11f9c-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="11f9c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="11f9c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="11f9c-112">Parameters</span></span>

 <span data-ttu-id="11f9c-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="11f9c-113">_cntf_</span></span>
  
> <span data-ttu-id="11f9c-114">[in] Число структур [УВЕДОМЛЕНИЙ](notification.md) в массива, указанного в параметре _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="11f9c-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="11f9c-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="11f9c-115">_rgntf_</span></span>
  
> <span data-ttu-id="11f9c-116">[in] Указатель на массив структур **УВЕДОМЛЕНИЙ** , размер которого является будет определено.</span><span class="sxs-lookup"><span data-stu-id="11f9c-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="11f9c-117">_печатной_</span><span class="sxs-lookup"><span data-stu-id="11f9c-117">_pcb_</span></span>
  
> <span data-ttu-id="11f9c-118">[out] Необязательный указатель на размер, в байтах, массива, на который указывает параметр _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="11f9c-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="11f9c-119">Если значение NULL, **ScCountNotifications** проверяет массива уведомлений.</span><span class="sxs-lookup"><span data-stu-id="11f9c-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="11f9c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11f9c-120">Return value</span></span>

<span data-ttu-id="11f9c-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="11f9c-121">S_OK</span></span>
  
> <span data-ttu-id="11f9c-122">Число успешно определены.</span><span class="sxs-lookup"><span data-stu-id="11f9c-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="11f9c-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="11f9c-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="11f9c-124">Обнаружен недопустимый уведомлений.</span><span class="sxs-lookup"><span data-stu-id="11f9c-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11f9c-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="11f9c-125">Remarks</span></span>

<span data-ttu-id="11f9c-126">Если с помощью параметра _печатной_ передано значение NULL, функция **ScCountNotifications** проверяет только массива уведомления, но не подсчет выполняется; Если ненулевое значение передается в _печатной_, **ScCountNotifications** определяет размер массива и сохраняет несколько _печатной_.</span><span class="sxs-lookup"><span data-stu-id="11f9c-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="11f9c-127">Параметр _печатной_ должен быть достаточно большим для размещения всего массива.</span><span class="sxs-lookup"><span data-stu-id="11f9c-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

