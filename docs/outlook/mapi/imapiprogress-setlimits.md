---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 14abfaadcdb1710a7cb8275c8f82d502aea8300e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809018"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="4fdff-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4fdff-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="4fdff-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fdff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fdff-105">Задает нижний и верхний ограничения на число элементов в операции и флаги, определяющие порядок вычисления сведения о ходе выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4fdff-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4fdff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fdff-106">Parameters</span></span>

 <span data-ttu-id="4fdff-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="4fdff-107">_lpulMin_</span></span>
  
> <span data-ttu-id="4fdff-108">[in] Указатель на переменную, содержащую нижнего предела элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="4fdff-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="4fdff-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="4fdff-109">_lpulMax_</span></span>
  
> <span data-ttu-id="4fdff-110">[in] Указатель на переменную, содержащую верхний предел элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="4fdff-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="4fdff-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fdff-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="4fdff-112">[in] Битовая маска флаги, определяющее уровень операции, на какие хода выполнения рассчитывается сведения.</span><span class="sxs-lookup"><span data-stu-id="4fdff-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="4fdff-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="4fdff-113">The following flag can be set:</span></span>
    
<span data-ttu-id="4fdff-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="4fdff-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="4fdff-115">Использует значения параметров метода [IMAPIProgress::Progress](imapiprogress-progress.md) _инициализирует метод ulCount_ и _ulTotal_ , которые указывают, в настоящее время обработанные элемента и всего элементов, соответственно, для увеличения ход выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4fdff-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="4fdff-116">Этот флаг установлен, значения глобального ограничены после должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="4fdff-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4fdff-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4fdff-117">Return value</span></span>

<span data-ttu-id="4fdff-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4fdff-118">S_OK</span></span> 
  
> <span data-ttu-id="4fdff-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4fdff-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4fdff-120">���������</span><span class="sxs-lookup"><span data-stu-id="4fdff-120">Remarks</span></span>

<span data-ttu-id="4fdff-121">Поставщики услуг вызовите метод **IMAPIProgress::SetLimits** установить или сбросить флаг MAPI_TOP_LEVEL и задавать локальных и глобальных минимального и максимального значения.</span><span class="sxs-lookup"><span data-stu-id="4fdff-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="4fdff-122">Значение параметра флаг влияет на объект хода выполнения понимает минимального и максимального значения для локальной или глобальной.</span><span class="sxs-lookup"><span data-stu-id="4fdff-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="4fdff-123">Если для флага MAPI_TOP_LEVEL, эти значения считаются глобальные и используются для вычисления хода выполнения для всей операции.</span><span class="sxs-lookup"><span data-stu-id="4fdff-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="4fdff-124">Объекты хода выполнения инициализации глобального минимальное значение 1 и глобальные максимальное значение до 1000.</span><span class="sxs-lookup"><span data-stu-id="4fdff-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="4fdff-125">При MAPI_TOP_LEVEL не задано, минимального и максимального значения считаются локальной и поставщики их использовать во внутренней сети для отображения хода выполнения для вложенных нижнем уровне.</span><span class="sxs-lookup"><span data-stu-id="4fdff-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="4fdff-126">Объекты хода выполнения сохраните локальные минимального и максимального значения только для того, чтобы они могут быть возвращены для поставщиков при вызове методов [IMAPIProgress::GetMin](imapiprogress-getmin.md) и [IMAPIProgress::GetMax](imapiprogress-getmax.md) .</span><span class="sxs-lookup"><span data-stu-id="4fdff-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="4fdff-127">Дополнительные сведения о том, как реализовать **SetLimits** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.</span><span class="sxs-lookup"><span data-stu-id="4fdff-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="4fdff-128">Дополнительные сведения о том, как и когда следует выполнять вызовы объект о ходе выполнения в разделе [отображаемое индикатор хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4fdff-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4fdff-129">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="4fdff-129">MFCMAPI reference</span></span>

<span data-ttu-id="4fdff-130">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="4fdff-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4fdff-131">**����**</span><span class="sxs-lookup"><span data-stu-id="4fdff-131">**File**</span></span>|<span data-ttu-id="4fdff-132">**�������**</span><span class="sxs-lookup"><span data-stu-id="4fdff-132">**Function**</span></span>|<span data-ttu-id="4fdff-133">**�����������**</span><span class="sxs-lookup"><span data-stu-id="4fdff-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4fdff-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="4fdff-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="4fdff-135">CMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4fdff-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="4fdff-136">Mfcmapi (en) использует метод **IMAPIProgress::SetLimits** для задания верхний и нижний предел и флаги для объекта хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4fdff-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fdff-137">См. также</span><span class="sxs-lookup"><span data-stu-id="4fdff-137">See also</span></span>



[<span data-ttu-id="4fdff-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="4fdff-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="4fdff-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="4fdff-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="4fdff-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="4fdff-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="4fdff-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fdff-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="4fdff-142">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="4fdff-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4fdff-143">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="4fdff-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="4fdff-144">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="4fdff-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

