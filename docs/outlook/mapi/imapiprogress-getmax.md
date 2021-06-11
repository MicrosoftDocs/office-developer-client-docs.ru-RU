---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436204"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="94015-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="94015-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="94015-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94015-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94015-105">Возвращает максимальное количество элементов в операции, для которой отображаются сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="94015-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="94015-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="94015-106">Parameters</span></span>

 <span data-ttu-id="94015-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="94015-107">_lpulMax_</span></span>
  
> <span data-ttu-id="94015-108">[вышел] Указатель на максимальное количество элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="94015-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94015-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94015-109">Return value</span></span>

<span data-ttu-id="94015-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="94015-110">S_OK</span></span> 
  
> <span data-ttu-id="94015-111">Максимальное количество элементов в операции было извлечено.</span><span class="sxs-lookup"><span data-stu-id="94015-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94015-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="94015-112">Remarks</span></span>

<span data-ttu-id="94015-113">Максимальное значение представляет окончание операции в числовом виде.</span><span class="sxs-lookup"><span data-stu-id="94015-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="94015-114">Оно может быть глобальным максимальным значением, представляющим отображаемые данные всего хода выполнения, или локальным значением, представляющим только часть отображаемых данных.</span><span class="sxs-lookup"><span data-stu-id="94015-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="94015-115">Значение параметра флага влияет на то, понимает ли объект progress максимальное значение локального или глобального значения.</span><span class="sxs-lookup"><span data-stu-id="94015-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="94015-116">При MAPI_TOP_LEVEL флаге максимальное значение считается глобальным и используется для вычисления хода всей операции.</span><span class="sxs-lookup"><span data-stu-id="94015-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="94015-117">Если MAPI_TOP_LEVEL не установлено, максимальное значение считается локальным, и поставщики используют его для отображения прогресса для подобектов нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="94015-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="94015-118">Объекты progress сэкономят локальное максимальное значение только для того, чтобы вернуть его поставщику с помощью **вызова GetMax.**</span><span class="sxs-lookup"><span data-stu-id="94015-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="94015-119">Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="94015-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="94015-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="94015-120">Notes to implementers</span></span>

<span data-ttu-id="94015-121">Инициализировать максимальное значение до 1000.</span><span class="sxs-lookup"><span data-stu-id="94015-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="94015-122">Поставщики службы могут сбросить это значение путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md).</span><span class="sxs-lookup"><span data-stu-id="94015-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="94015-123">Дополнительные сведения о том, как реализовать **GetMax** и другие методы [IMAPIProgress,](imapiprogressiunknown.md) см. в дополнительных сведениях о [реализации индикатора прогресса.](implementing-a-progress-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="94015-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="94015-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="94015-124">MFCMAPI reference</span></span>

<span data-ttu-id="94015-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="94015-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="94015-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="94015-126">**File**</span></span>|<span data-ttu-id="94015-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="94015-127">**Function**</span></span>|<span data-ttu-id="94015-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="94015-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="94015-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="94015-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="94015-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="94015-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="94015-131">MFCMAPI использует **метод IMAPIProgress::GetMax,** чтобы получить максимальное значение для объекта progress.</span><span class="sxs-lookup"><span data-stu-id="94015-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="94015-132">Возвращает 1000, если ранее не были установлены ограничения с помощью метода **IMAPIProgress::SetLimits.**</span><span class="sxs-lookup"><span data-stu-id="94015-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94015-133">См. также</span><span class="sxs-lookup"><span data-stu-id="94015-133">See also</span></span>



[<span data-ttu-id="94015-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="94015-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="94015-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="94015-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="94015-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="94015-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="94015-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94015-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="94015-138">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="94015-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="94015-139">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="94015-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="94015-140">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="94015-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

