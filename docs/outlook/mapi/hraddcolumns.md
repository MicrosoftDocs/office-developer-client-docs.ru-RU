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
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422476"
---
# <a name="hraddcolumns"></a><span data-ttu-id="a0694-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="a0694-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="a0694-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0694-105">Добавляет или перемещает столбцы в начало существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="a0694-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0694-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a0694-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0694-107">мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="a0694-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a0694-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a0694-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0694-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a0694-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a0694-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a0694-110">Called by:</span></span>  <br/> |<span data-ttu-id="a0694-111">Клиентские приложения и поставщики услуг.</span><span class="sxs-lookup"><span data-stu-id="a0694-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="a0694-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0694-112">Parameters</span></span>

 <span data-ttu-id="a0694-113">_лптбл_</span><span class="sxs-lookup"><span data-stu-id="a0694-113">_lptbl_</span></span>
  
> <span data-ttu-id="a0694-114">возврата Указатель на таблицу MAPI, на которую вы затронули.</span><span class="sxs-lookup"><span data-stu-id="a0694-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="a0694-115">_Лппроптагколумнснев_</span><span class="sxs-lookup"><span data-stu-id="a0694-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="a0694-116">возврата Указатель на структуру **спроптагаррай** , которая содержит массив тегов свойств для добавления или перемещения свойств в начало таблицы.</span><span class="sxs-lookup"><span data-stu-id="a0694-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="a0694-117">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="a0694-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a0694-118">возврата Указатель на функцию **мапиаллокатебуффер** .</span><span class="sxs-lookup"><span data-stu-id="a0694-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="a0694-119">Используется для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="a0694-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="a0694-120">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="a0694-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="a0694-121">возврата Указатель на функцию **мапифрибуффер** .</span><span class="sxs-lookup"><span data-stu-id="a0694-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="a0694-122">Используется для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="a0694-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a0694-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0694-123">Return value</span></span>

 <span data-ttu-id="a0694-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="a0694-124">**S_OK**</span></span>
  
> <span data-ttu-id="a0694-125">Вызов выполнен успешно, и указанные столбцы были перемещены или добавлены.</span><span class="sxs-lookup"><span data-stu-id="a0694-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0694-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0694-126">Remarks</span></span>

<span data-ttu-id="a0694-127">Функция **храддколумнс** эквивалентна использованию **храддколумнсекс** с параметром _лпфнфилтерколумнс_ , равным null.</span><span class="sxs-lookup"><span data-stu-id="a0694-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0694-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a0694-128">See also</span></span>



[<span data-ttu-id="a0694-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="a0694-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="a0694-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a0694-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a0694-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a0694-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a0694-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a0694-132">SPropTagArray</span></span>](sproptagarray.md)

