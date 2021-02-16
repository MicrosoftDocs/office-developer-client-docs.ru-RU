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
# <a name="screlocnotifications"></a><span data-ttu-id="cf978-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="cf978-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="cf978-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf978-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf978-105">Настраивает указатель в указанном массиве уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="cf978-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf978-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cf978-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf978-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cf978-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cf978-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cf978-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cf978-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cf978-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cf978-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cf978-110">Called by:</span></span>  <br/> |<span data-ttu-id="cf978-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="cf978-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="cf978-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf978-112">Parameters</span></span>

 <span data-ttu-id="cf978-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="cf978-113">_cntf_</span></span>
  
> <span data-ttu-id="cf978-114">[in] Количество структур [NOTIFICATION](notification.md) в массиве, указанных параметром _rgntf._</span><span class="sxs-lookup"><span data-stu-id="cf978-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="cf978-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="cf978-115">_rgntf_</span></span>
  
> <span data-ttu-id="cf978-116">[in] Указатель на массив  структур УВЕДОМЛЕНий, определяющих уведомления о событиях, в которых необходимо скорректировать указатель.</span><span class="sxs-lookup"><span data-stu-id="cf978-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="cf978-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="cf978-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="cf978-118">[in] Указатель на исходный базовый адрес массива, указанный _параметром rgntf._</span><span class="sxs-lookup"><span data-stu-id="cf978-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="cf978-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="cf978-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="cf978-120">[in] Расположение, в которое **ScRelocNotifications** записывает новый базовый адрес массива, указанный параметром _rgntf._</span><span class="sxs-lookup"><span data-stu-id="cf978-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="cf978-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="cf978-121">_pcb_</span></span>
  
> <span data-ttu-id="cf978-122">[out] Указатель на размер массива в вайтах, указанный параметром _pvBaseNew._</span><span class="sxs-lookup"><span data-stu-id="cf978-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cf978-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf978-123">Return value</span></span>

<span data-ttu-id="cf978-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf978-124">S_OK</span></span>
  
> <span data-ttu-id="cf978-125">Указатель успешно настроен.</span><span class="sxs-lookup"><span data-stu-id="cf978-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="cf978-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cf978-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="cf978-127">Было выявилось недопустимое уведомление.</span><span class="sxs-lookup"><span data-stu-id="cf978-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf978-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf978-128">Remarks</span></span>

<span data-ttu-id="cf978-129">Параметр  _pcb_ для **функции ScRelocNotifications** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cf978-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf978-130">См. также</span><span class="sxs-lookup"><span data-stu-id="cf978-130">See also</span></span>



[<span data-ttu-id="cf978-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="cf978-131">ScRelocProps</span></span>](screlocprops.md)

