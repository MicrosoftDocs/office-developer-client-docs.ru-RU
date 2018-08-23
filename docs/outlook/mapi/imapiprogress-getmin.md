---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cff866ce73eb6ada45a2b629a6c95c69ad189045
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587826"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="bcec1-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="bcec1-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="bcec1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcec1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcec1-105">Возвращает минимальное значение в метод [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) , для которых выполняется отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="bcec1-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="bcec1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcec1-106">Parameters</span></span>

 <span data-ttu-id="bcec1-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="bcec1-107">_lpulMin_</span></span>
  
> <span data-ttu-id="bcec1-108">[out] Указатель на минимальное число элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="bcec1-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcec1-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bcec1-109">Return value</span></span>

<span data-ttu-id="bcec1-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="bcec1-110">S_OK</span></span> 
  
> <span data-ttu-id="bcec1-111">Минимальное число элементов в операции были получены.</span><span class="sxs-lookup"><span data-stu-id="bcec1-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcec1-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="bcec1-112">Remarks</span></span>

<span data-ttu-id="bcec1-113">Минимальное значение представляет начало операции в числовой форме.</span><span class="sxs-lookup"><span data-stu-id="bcec1-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="bcec1-114">Значение может быть глобальной максимальное значение, используемый для представления области отображения всей хода выполнения или локальное значение, используемый для представления только часть отображения.</span><span class="sxs-lookup"><span data-stu-id="bcec1-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="bcec1-115">Значение параметра флаг влияет на объект хода выполнения понимает минимальное значение локальной или глобальной.</span><span class="sxs-lookup"><span data-stu-id="bcec1-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="bcec1-116">Если для флага MAPI_TOP_LEVEL, минимальное значение считается глобальный и используется для вычисления хода выполнения для всей операции.</span><span class="sxs-lookup"><span data-stu-id="bcec1-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="bcec1-117">При MAPI_TOP_LEVEL не задано, минимальное значение считается локальной и поставщики используют во внутренней сети для отображения хода выполнения для вложенных нижнем уровне.</span><span class="sxs-lookup"><span data-stu-id="bcec1-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="bcec1-118">Объекты хода выполнения сохраните локального минимальное значение только для возвращения к поставщику посредством вызова **GetMin** .</span><span class="sxs-lookup"><span data-stu-id="bcec1-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bcec1-119">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="bcec1-119">Notes to implementers</span></span>

<span data-ttu-id="bcec1-120">Инициализация минимальное значение 1.</span><span class="sxs-lookup"><span data-stu-id="bcec1-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="bcec1-121">Поставщиков услуг может сбросить это значение путем вызова метода **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="bcec1-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="bcec1-122">Дополнительные сведения о том, как реализовать **GetMin** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.</span><span class="sxs-lookup"><span data-stu-id="bcec1-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="bcec1-123">Дополнительные сведения о том, как и когда следует выполнять вызовы объект о ходе выполнения в разделе [отображаемое индикатор хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="bcec1-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bcec1-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="bcec1-124">MFCMAPI reference</span></span>

<span data-ttu-id="bcec1-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="bcec1-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bcec1-126">**����**</span><span class="sxs-lookup"><span data-stu-id="bcec1-126">**File**</span></span>|<span data-ttu-id="bcec1-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="bcec1-127">**Function**</span></span>|<span data-ttu-id="bcec1-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="bcec1-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bcec1-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="bcec1-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="bcec1-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="bcec1-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="bcec1-131">Mfcmapi (en) использует метод **IMAPIProgress::GetMin** для получения минимальное значение для индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="bcec1-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="bcec1-132">Возвращает значение 1, если не ограничения ранее были установлены путем вызова метода **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="bcec1-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcec1-133">См. также</span><span class="sxs-lookup"><span data-stu-id="bcec1-133">See also</span></span>



[<span data-ttu-id="bcec1-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="bcec1-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="bcec1-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="bcec1-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="bcec1-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="bcec1-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="bcec1-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcec1-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="bcec1-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bcec1-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="bcec1-139">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="bcec1-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="bcec1-140">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="bcec1-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

