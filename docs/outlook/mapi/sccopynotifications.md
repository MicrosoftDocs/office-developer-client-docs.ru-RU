---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7d4877c81a52b529aa183ea552430b481c6617f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593356"
---
# <a name="sccopynotifications"></a><span data-ttu-id="ca80f-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="ca80f-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="ca80f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca80f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca80f-105">Группа уведомлений о событиях копируется на один блок памяти.</span><span class="sxs-lookup"><span data-stu-id="ca80f-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca80f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ca80f-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca80f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ca80f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ca80f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ca80f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ca80f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ca80f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ca80f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ca80f-110">Called by:</span></span>  <br/> |<span data-ttu-id="ca80f-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ca80f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="ca80f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca80f-112">Parameters</span></span>

 <span data-ttu-id="ca80f-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="ca80f-113">_cntf_</span></span>
  
> <span data-ttu-id="ca80f-114">[in] Число структур [УВЕДОМЛЕНИЙ](notification.md) в массива, указанного в параметре _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="ca80f-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="ca80f-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="ca80f-115">_rgntf_</span></span>
  
> <span data-ttu-id="ca80f-116">[in] Указатель на массив структур **УВЕДОМЛЕНИЙ** , определение уведомления о событиях для копирования.</span><span class="sxs-lookup"><span data-stu-id="ca80f-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="ca80f-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="ca80f-117">_pvDst_</span></span>
  
> <span data-ttu-id="ca80f-118">[out] Указатель на возвращенные уведомления.</span><span class="sxs-lookup"><span data-stu-id="ca80f-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="ca80f-119">_печатной_</span><span class="sxs-lookup"><span data-stu-id="ca80f-119">_pcb_</span></span>
  
> <span data-ttu-id="ca80f-120">[out] Необязательный указатель на переменную, где размер в байтах, массива, на который указывает с помощью параметра _rgntf_ сохраняется.</span><span class="sxs-lookup"><span data-stu-id="ca80f-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="ca80f-121">Если это не имеет значение NULL, параметр _печатной_ число байтов, сохраненных в параметре _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="ca80f-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca80f-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca80f-122">Return value</span></span>

<span data-ttu-id="ca80f-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca80f-123">S_OK</span></span>
  
> <span data-ttu-id="ca80f-124">Уведомления о событиях были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="ca80f-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="ca80f-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ca80f-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="ca80f-126">Обнаружен недопустимый уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ca80f-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca80f-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca80f-127">Remarks</span></span>

<span data-ttu-id="ca80f-128">Если в параметре _печатной_ передано значение NULL, не копирование не выполняется. Если ненулевое значение передается в _печатной_, функция **ScCopyNotifications** копирует размер массива и самого массива на один блок памяти.</span><span class="sxs-lookup"><span data-stu-id="ca80f-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="ca80f-129">Если _печатной_ не равно NULL, перейдут в число байтов, сохраненных в параметре _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="ca80f-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="ca80f-130">Параметр _pvDst_ должен быть достаточно большим для размещения всего массива.</span><span class="sxs-lookup"><span data-stu-id="ca80f-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

