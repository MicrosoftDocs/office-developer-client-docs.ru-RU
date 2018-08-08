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
ms.openlocfilehash: bbd52116a108be12df7697f45df41b03adeba68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809010"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="4804c-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="4804c-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="4804c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4804c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4804c-105">Возвращает максимальное число элементов в операции, для которых выполняется отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="4804c-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="4804c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4804c-106">Parameters</span></span>

 <span data-ttu-id="4804c-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="4804c-107">_lpulMax_</span></span>
  
> <span data-ttu-id="4804c-108">[out] Указатель на максимальное число элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="4804c-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4804c-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4804c-109">Return value</span></span>

<span data-ttu-id="4804c-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4804c-110">S_OK</span></span> 
  
> <span data-ttu-id="4804c-111">Максимальное число элементов в операции были получены.</span><span class="sxs-lookup"><span data-stu-id="4804c-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4804c-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="4804c-112">Remarks</span></span>

<span data-ttu-id="4804c-113">Максимальное значение представляет конец операции в числовой форме.</span><span class="sxs-lookup"><span data-stu-id="4804c-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="4804c-114">Значение может быть глобальной максимальное значение, используемый для представления области отображения всей хода выполнения или локальное значение, используемый для представления только часть отображения.</span><span class="sxs-lookup"><span data-stu-id="4804c-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="4804c-115">Значение параметра флаг влияет на объект хода выполнения понимает максимальное значение, которое необходимо локальной или глобальной.</span><span class="sxs-lookup"><span data-stu-id="4804c-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="4804c-116">Если для флага MAPI_TOP_LEVEL, максимальное значение считается глобальный и используется для вычисления хода выполнения для всей операции.</span><span class="sxs-lookup"><span data-stu-id="4804c-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="4804c-117">При MAPI_TOP_LEVEL не задано, максимальное значение считается локальной и поставщики используют во внутренней сети для отображения хода выполнения для вложенных нижнем уровне.</span><span class="sxs-lookup"><span data-stu-id="4804c-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="4804c-118">Объекты хода выполнения сохраните локального максимальное значение только для возвращения к поставщику посредством вызова **GetMax** .</span><span class="sxs-lookup"><span data-stu-id="4804c-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="4804c-119">Дополнительные сведения о том, как и когда следует выполнять вызовы объект о ходе выполнения в разделе [отображаемое индикатор хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4804c-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4804c-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="4804c-120">Notes to implementers</span></span>

<span data-ttu-id="4804c-121">Инициализация максимальное значение до 1000.</span><span class="sxs-lookup"><span data-stu-id="4804c-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="4804c-122">Поставщиков услуг может сбросить это значение путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="4804c-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="4804c-123">Дополнительные сведения о том, как реализовать **GetMax** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.</span><span class="sxs-lookup"><span data-stu-id="4804c-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4804c-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="4804c-124">MFCMAPI reference</span></span>

<span data-ttu-id="4804c-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="4804c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4804c-126">**����**</span><span class="sxs-lookup"><span data-stu-id="4804c-126">**File**</span></span>|<span data-ttu-id="4804c-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="4804c-127">**Function**</span></span>|<span data-ttu-id="4804c-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="4804c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4804c-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="4804c-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="4804c-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="4804c-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="4804c-131">Mfcmapi (en) использует метод **IMAPIProgress::GetMax** для получения максимального значения для объекта хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4804c-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="4804c-132">Возвращает 1000, если только с помощью метода **IMAPIProgress::SetLimits** ранее были установлены ограничения.</span><span class="sxs-lookup"><span data-stu-id="4804c-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4804c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="4804c-133">See also</span></span>



[<span data-ttu-id="4804c-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="4804c-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="4804c-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="4804c-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="4804c-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4804c-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="4804c-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4804c-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="4804c-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="4804c-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4804c-139">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="4804c-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="4804c-140">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="4804c-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

