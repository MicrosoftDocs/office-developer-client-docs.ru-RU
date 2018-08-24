---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580735"
---
# <a name="hraddcolumns"></a><span data-ttu-id="bdf5f-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="bdf5f-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="bdf5f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdf5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdf5f-105">Добавляет или перемещение столбцов в начало существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bdf5f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bdf5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="bdf5f-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bdf5f-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bdf5f-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="bdf5f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bdf5f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bdf5f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bdf5f-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="bdf5f-110">Called by:</span></span>  <br/> |<span data-ttu-id="bdf5f-111">Клиентские приложения и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="bdf5f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdf5f-112">Parameters</span></span>

 <span data-ttu-id="bdf5f-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="bdf5f-113">_lptbl_</span></span>
  
> <span data-ttu-id="bdf5f-114">[in] Указатель на влияет на таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="bdf5f-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="bdf5f-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="bdf5f-116">[in] Указатель на структуру **SPropTagArray** , который содержит массив теги свойства для свойств для добавления или перемещения в начало таблицы.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="bdf5f-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="bdf5f-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="bdf5f-118">[in] Указатель на функцию **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="bdf5f-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="bdf5f-119">Используется для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="bdf5f-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="bdf5f-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="bdf5f-121">[in] Указатель на функцию **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="bdf5f-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="bdf5f-122">Используется, чтобы освободить память.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bdf5f-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bdf5f-123">Return value</span></span>

 <span data-ttu-id="bdf5f-124">**ЗНАЧЕНИЕ S_OK**</span><span class="sxs-lookup"><span data-stu-id="bdf5f-124">**S_OK**</span></span>
  
> <span data-ttu-id="bdf5f-125">Вызов завершился успешно и были перемещены или добавить указанных столбцов.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bdf5f-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="bdf5f-126">Remarks</span></span>

<span data-ttu-id="bdf5f-127">Функция **HrAddColumns** эквивалентно использованию **HrAddColumnsEx** с _lpfnFilterColumns_ задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bdf5f-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bdf5f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bdf5f-128">See also</span></span>



[<span data-ttu-id="bdf5f-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="bdf5f-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="bdf5f-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="bdf5f-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="bdf5f-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bdf5f-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bdf5f-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="bdf5f-132">SPropTagArray</span></span>](sproptagarray.md)

