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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351374"
---
# <a name="sccountnotifications"></a><span data-ttu-id="60c9d-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="60c9d-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="60c9d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60c9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60c9d-105">Определяет размер (в байтах) массива уведомлений о событиях и проверяет память, связанную с массивом.</span><span class="sxs-lookup"><span data-stu-id="60c9d-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60c9d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="60c9d-106">Header file:</span></span>  <br/> |<span data-ttu-id="60c9d-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="60c9d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="60c9d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="60c9d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="60c9d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="60c9d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="60c9d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="60c9d-110">Called by:</span></span>  <br/> |<span data-ttu-id="60c9d-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="60c9d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="60c9d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="60c9d-112">Parameters</span></span>

 <span data-ttu-id="60c9d-113">_кнтф_</span><span class="sxs-lookup"><span data-stu-id="60c9d-113">_cntf_</span></span>
  
> <span data-ttu-id="60c9d-114">возврата Количество структур [уведомлений](notification.md) в массиве, указанном с помощью параметра _ргнтф_ .</span><span class="sxs-lookup"><span data-stu-id="60c9d-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="60c9d-115">_ргнтф_</span><span class="sxs-lookup"><span data-stu-id="60c9d-115">_rgntf_</span></span>
  
> <span data-ttu-id="60c9d-116">возврата Указатель на массив структур **уведомлений** , размер которых необходимо определить.</span><span class="sxs-lookup"><span data-stu-id="60c9d-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="60c9d-117">_ПКБ_</span><span class="sxs-lookup"><span data-stu-id="60c9d-117">_pcb_</span></span>
  
> <span data-ttu-id="60c9d-118">вышли НеОбязательный указатель размера массива (в байтах), на который указывает параметр _ргнтф_ .</span><span class="sxs-lookup"><span data-stu-id="60c9d-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="60c9d-119">Если значение равно NULL, **сккаунтнотификатионс** проверяет массив уведомлений.</span><span class="sxs-lookup"><span data-stu-id="60c9d-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="60c9d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60c9d-120">Return value</span></span>

<span data-ttu-id="60c9d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="60c9d-121">S_OK</span></span>
  
> <span data-ttu-id="60c9d-122">Число успешно определено.</span><span class="sxs-lookup"><span data-stu-id="60c9d-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="60c9d-123">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="60c9d-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="60c9d-124">Обнаружено недопустимое уведомление.</span><span class="sxs-lookup"><span data-stu-id="60c9d-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60c9d-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="60c9d-125">Remarks</span></span>

<span data-ttu-id="60c9d-126">Если в параметре _ПКБ_ переДАЕТСЯ значение null, функция **сккаунтнотификатионс** только проверяет массив уведомлений, но подсчет не выполняется; Если в _ПКБ_передается значение, отличное от NULL, **сккаунтнотификатионс** определяет размер массива и сохраняет ошибку _ПКБ_.</span><span class="sxs-lookup"><span data-stu-id="60c9d-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="60c9d-127">Параметр _ПКБ_ должен быть достаточно большим, чтобы вместить весь массив.</span><span class="sxs-lookup"><span data-stu-id="60c9d-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

