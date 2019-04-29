---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415203"
---
# <a name="screlocnotifications"></a><span data-ttu-id="d2ca0-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="d2ca0-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="d2ca0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2ca0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2ca0-105">НаСтраивает указатель в пределах указанного массива уведомлений о событии.</span><span class="sxs-lookup"><span data-stu-id="d2ca0-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2ca0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d2ca0-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2ca0-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="d2ca0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d2ca0-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d2ca0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2ca0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2ca0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2ca0-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d2ca0-110">Called by:</span></span>  <br/> |<span data-ttu-id="d2ca0-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d2ca0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="d2ca0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2ca0-112">Parameters</span></span>

 <span data-ttu-id="d2ca0-113">_кнтф_</span><span class="sxs-lookup"><span data-stu-id="d2ca0-113">_cntf_</span></span>
  
> <span data-ttu-id="d2ca0-114">возврата Количество структур [уведомлений](notification.md) в массиве, указанном с помощью параметра _ргнтф_ .</span><span class="sxs-lookup"><span data-stu-id="d2ca0-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d2ca0-115">_ргнтф_</span><span class="sxs-lookup"><span data-stu-id="d2ca0-115">_rgntf_</span></span>
  
> <span data-ttu-id="d2ca0-116">возврата Указатель на массив структур **уведомлений** , определяющий уведомления о событиях, в которых будет корректироваться указатель.</span><span class="sxs-lookup"><span data-stu-id="d2ca0-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="d2ca0-117">_Пвбасеолд_</span><span class="sxs-lookup"><span data-stu-id="d2ca0-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="d2ca0-118">возврата Указатель на исходный базовый адрес массива, указанного параметром _ргнтф_ .</span><span class="sxs-lookup"><span data-stu-id="d2ca0-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d2ca0-119">_Пвбасенев_</span><span class="sxs-lookup"><span data-stu-id="d2ca0-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="d2ca0-120">возврата Расположение, в которое **скрелокнотификатионс** записывает новый базовый адрес массива, указанного с помощью параметра _ргнтф_ .</span><span class="sxs-lookup"><span data-stu-id="d2ca0-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d2ca0-121">_ПКБ_</span><span class="sxs-lookup"><span data-stu-id="d2ca0-121">_pcb_</span></span>
  
> <span data-ttu-id="d2ca0-122">вышли Указатель на размер массива (в байтах), указанный параметром _пвбасенев_ .</span><span class="sxs-lookup"><span data-stu-id="d2ca0-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d2ca0-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2ca0-123">Return value</span></span>

<span data-ttu-id="d2ca0-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2ca0-124">S_OK</span></span>
  
> <span data-ttu-id="d2ca0-125">Указатель был успешно изменен.</span><span class="sxs-lookup"><span data-stu-id="d2ca0-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="d2ca0-126">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="d2ca0-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="d2ca0-127">Обнаружено недопустимое уведомление.</span><span class="sxs-lookup"><span data-stu-id="d2ca0-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2ca0-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2ca0-128">Remarks</span></span>

<span data-ttu-id="d2ca0-129">Параметр _ПКБ_ для функции **скрелокнотификатионс** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d2ca0-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2ca0-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d2ca0-130">See also</span></span>



[<span data-ttu-id="d2ca0-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="d2ca0-131">ScRelocProps</span></span>](screlocprops.md)

