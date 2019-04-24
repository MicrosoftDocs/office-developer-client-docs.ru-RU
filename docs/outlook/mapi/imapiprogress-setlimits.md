---
title: Имапипрогресссетлимитс
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
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339867"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="fe2ba-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="fe2ba-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="fe2ba-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe2ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe2ba-105">Задает нижний и верхний пределы числа элементов в операции, а также флаги, которые контролируют способ вычисления сведений о ходе выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fe2ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe2ba-106">Parameters</span></span>

 <span data-ttu-id="fe2ba-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="fe2ba-107">_lpulMin_</span></span>
  
> <span data-ttu-id="fe2ba-108">возврата Указатель на переменную, которая содержит нижний предел элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="fe2ba-109">_Лпулмакс_</span><span class="sxs-lookup"><span data-stu-id="fe2ba-109">_lpulMax_</span></span>
  
> <span data-ttu-id="fe2ba-110">возврата Указатель на переменную, которая содержит верхний предел элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="fe2ba-111">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="fe2ba-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="fe2ba-112">возврата Битовая маска флагов, которые управляют уровнем работы, на котором рассчитываются сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="fe2ba-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fe2ba-113">The following flag can be set:</span></span>
    
<span data-ttu-id="fe2ba-114">МАПИ_ТОП_ЛЕВЕЛ</span><span class="sxs-lookup"><span data-stu-id="fe2ba-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="fe2ba-115">Использует значения в параметрах _улкаунт_ и _ултотал_ метода [IMAPIProgress::P рогресс](imapiprogress-progress.md) , которые указывают текущий обрабатываемый элемент и общее количество элементов, соответственно, для увеличения хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="fe2ba-116">При установке этого флага необходимо задать значения глобальных нижних и верхних пределов.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe2ba-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe2ba-117">Return value</span></span>

<span data-ttu-id="fe2ba-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe2ba-118">S_OK</span></span> 
  
> <span data-ttu-id="fe2ba-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe2ba-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe2ba-120">Remarks</span></span>

<span data-ttu-id="fe2ba-121">Поставщики услуг вызывают метод **IMAPIProgress:: SetLimits** для установки или снятия ФЛАГа мапи_топ_левел, а также для задания локальных и глобальных минимальных и максимальных значений.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="fe2ba-122">Значение параметра flag влияет на то, что объект Progress понимает минимальное и максимальное значения, которые должны быть локальными или глобальными.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="fe2ba-123">Если установлен флаг МАПИ_ТОП_ЛЕВЕЛ, эти значения считаются глобальными и используются для вычисления хода выполнения для всей операции.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="fe2ba-124">Объекты хода выполнения инициализируют глобальное минимальное значение 1, а глобальное максимальное значение — на 1000.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="fe2ba-125">Если МАПИ_ТОП_ЛЕВЕЛ не задано, то минимальное и максимальное значения считаются локальным, а поставщики используют их для внутренних целей для отображения хода выполнения для подобъектов нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="fe2ba-126">Объекты хода выполнения сохраняют локальное минимальное и максимальное значения только для того, чтобы их можно было возвратить поставщикам при вызове методов [IMAPIProgress:: GetMin](imapiprogress-getmin.md) и [IMAPIProgress:: жетмакс](imapiprogress-getmax.md) .</span><span class="sxs-lookup"><span data-stu-id="fe2ba-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="fe2ba-127">Дополнительные сведения о том, как реализовать **SetLimits** и другие методы [IMAPIProgress](imapiprogressiunknown.md) , можно найти в разделе [Реализация индикатора хода выполнения](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="fe2ba-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="fe2ba-128">Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="fe2ba-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fe2ba-129">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fe2ba-129">MFCMAPI reference</span></span>

<span data-ttu-id="fe2ba-130">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fe2ba-131">**Файл**</span><span class="sxs-lookup"><span data-stu-id="fe2ba-131">**File**</span></span>|<span data-ttu-id="fe2ba-132">**Функция**</span><span class="sxs-lookup"><span data-stu-id="fe2ba-132">**Function**</span></span>|<span data-ttu-id="fe2ba-133">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="fe2ba-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe2ba-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="fe2ba-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="fe2ba-135">Кмапипрогресс:: SetLimits</span><span class="sxs-lookup"><span data-stu-id="fe2ba-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="fe2ba-136">MFCMAPI использует метод **IMAPIProgress:: SetLimits** для установки максимальных и минимальных пределов и флагов для объекта хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fe2ba-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe2ba-137">См. также</span><span class="sxs-lookup"><span data-stu-id="fe2ba-137">See also</span></span>



[<span data-ttu-id="fe2ba-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="fe2ba-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="fe2ba-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="fe2ba-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="fe2ba-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="fe2ba-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="fe2ba-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe2ba-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="fe2ba-142">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="fe2ba-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fe2ba-143">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="fe2ba-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="fe2ba-144">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="fe2ba-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

