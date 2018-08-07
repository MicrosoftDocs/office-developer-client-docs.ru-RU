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
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812240"
---
# <a name="screlocnotifications"></a><span data-ttu-id="15bff-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="15bff-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="15bff-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15bff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15bff-105">Изменяет указатель в массиве указанного события уведомления.</span><span class="sxs-lookup"><span data-stu-id="15bff-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15bff-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="15bff-106">Header file:</span></span>  <br/> |<span data-ttu-id="15bff-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="15bff-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="15bff-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="15bff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="15bff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="15bff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="15bff-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="15bff-110">Called by:</span></span>  <br/> |<span data-ttu-id="15bff-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="15bff-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="15bff-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="15bff-112">Parameters</span></span>

 <span data-ttu-id="15bff-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="15bff-113">_cntf_</span></span>
  
> <span data-ttu-id="15bff-114">[in] Число структур [УВЕДОМЛЕНИЙ](notification.md) в массива, указанного в параметре _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="15bff-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="15bff-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="15bff-115">_rgntf_</span></span>
  
> <span data-ttu-id="15bff-116">[in] Указатель на массив структур **УВЕДОМЛЕНИЙ** , определение уведомления о событиях, в течение которых является указатель для настройки.</span><span class="sxs-lookup"><span data-stu-id="15bff-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="15bff-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="15bff-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="15bff-118">[in] Указатель на исходный базовый адрес массива, указанного в параметре _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="15bff-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="15bff-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="15bff-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="15bff-120">[in] Расположение, к которому **ScRelocNotifications** записывает новый базовый адрес массива, указанного в параметре _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="15bff-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="15bff-121">_печатной_</span><span class="sxs-lookup"><span data-stu-id="15bff-121">_pcb_</span></span>
  
> <span data-ttu-id="15bff-122">[out] Указатель на размер, в байтах, массива, указанного в параметре _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="15bff-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15bff-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3">Return value</span></span>

<span data-ttu-id="15bff-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="15bff-124">S_OK</span></span>
  
> <span data-ttu-id="15bff-125">Указатель был успешно изменены.</span><span class="sxs-lookup"><span data-stu-id="15bff-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="15bff-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="15bff-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="15bff-127">Обнаружен недопустимый уведомлений.</span><span class="sxs-lookup"><span data-stu-id="15bff-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15bff-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="15bff-128">Remarks</span></span>

<span data-ttu-id="15bff-129">Это необязательный параметр _печатной_ в функцию **ScRelocNotifications** .</span><span class="sxs-lookup"><span data-stu-id="15bff-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15bff-130">См. также</span><span class="sxs-lookup"><span data-stu-id="15bff-130">See also</span></span>



[<span data-ttu-id="15bff-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="15bff-131">ScRelocProps</span></span>](screlocprops.md)

