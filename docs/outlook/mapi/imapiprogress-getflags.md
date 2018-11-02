---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a5e4205a808c7a6e469d2e9cb0a1b3c17a92d21
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573546"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="17df2-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="17df2-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="17df2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17df2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17df2-105">Возвращает флаг, параметры из объекта о ходе выполнения для уровня операции, на котором рассчитывается сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="17df2-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="17df2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17df2-106">Parameters</span></span>

 <span data-ttu-id="17df2-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="17df2-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="17df2-108">[out] Битовая маска флаги, определяющее уровень операции, на какие хода выполнения рассчитывается сведения.</span><span class="sxs-lookup"><span data-stu-id="17df2-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="17df2-109">Может быть возвращено следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="17df2-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="17df2-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="17df2-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="17df2-111">Ход выполнения рассчитывается для объекта верхнего уровня, объект, который будет вызываться клиентом для начала операции.</span><span class="sxs-lookup"><span data-stu-id="17df2-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="17df2-112">Например объект верхнего уровня в операцию копирования папки — это папка, которое выполняется копирование.</span><span class="sxs-lookup"><span data-stu-id="17df2-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="17df2-113">Если MAPI_TOP_LEVEL не задано, о ходе выполнения рассчитывается для нижнего уровня объекта или вложенные объекты.</span><span class="sxs-lookup"><span data-stu-id="17df2-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="17df2-114">В операцию копирования папки нижнего уровня объекта является одним из вложенных папок в папке, в которое выполняется копирование.</span><span class="sxs-lookup"><span data-stu-id="17df2-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17df2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17df2-115">Return value</span></span>

<span data-ttu-id="17df2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="17df2-116">S_OK</span></span> 
  
> <span data-ttu-id="17df2-117">Успешно возвращено значение флаги.</span><span class="sxs-lookup"><span data-stu-id="17df2-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17df2-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="17df2-118">Remarks</span></span>

<span data-ttu-id="17df2-119">MAPI поставщики услуг для различения объектов верхнего уровня и вложенных с флагом MAPI_TOP_LEVEL, чтобы все объекты задействованных в рамках одной операции можно использовать ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для отображения хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="17df2-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="17df2-120">В этом случае отображения индикатора осуществляются без проблем в одном направлении положительное.</span><span class="sxs-lookup"><span data-stu-id="17df2-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="17df2-121">Установлен ли флаг MAPI_TOP_LEVEL определяет, как поставщиков услуг задавать другие параметры в последующие запросы к объекту хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="17df2-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="17df2-122">Изначально принимает значение, возвращенное **GetFlags** средством реализации, а затем поставщиком услуг путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="17df2-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="17df2-123">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="17df2-123">Notes to implementers</span></span>

<span data-ttu-id="17df2-124">Всегда инициализировать флаг, MAPI_TOP_LEVEL и затем использовать поставщиков услуг, снимите его в случае необходимости.</span><span class="sxs-lookup"><span data-stu-id="17df2-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="17df2-125">Поставщиков услуг можно очистить и Сбросить флаг путем вызова метода **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="17df2-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="17df2-126">Дополнительные сведения о том, как реализовать **GetFlags** и другие методы **IMAPIProgress** [Индикатор выполнения](implementing-a-progress-indicator.md)см.</span><span class="sxs-lookup"><span data-stu-id="17df2-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="17df2-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="17df2-127">Notes to callers</span></span>

<span data-ttu-id="17df2-128">При отображении индикатор выполнения вызова первого звонка с **IMAPIProgress::GetFlags**.</span><span class="sxs-lookup"><span data-stu-id="17df2-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="17df2-129">Возвращаемое значение должно быть MAPI_TOP_LEVEL, так как все реализации инициализировать содержимое параметр _lpulFlags_ это значение.</span><span class="sxs-lookup"><span data-stu-id="17df2-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="17df2-130">Дополнительные сведения о последовательности вызовов объекта хода выполнения просмотрите [представление индикатор хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="17df2-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="17df2-131">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="17df2-131">MFCMAPI reference</span></span>

<span data-ttu-id="17df2-132">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="17df2-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="17df2-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="17df2-133">**File**</span></span>|<span data-ttu-id="17df2-134">**Функция**</span><span class="sxs-lookup"><span data-stu-id="17df2-134">**Function**</span></span>|<span data-ttu-id="17df2-135">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="17df2-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="17df2-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="17df2-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="17df2-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="17df2-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="17df2-138">Mfcmapi (en) использует метод **IMAPIProgress::GetFlags** , чтобы определить, какие флаги установлены.</span><span class="sxs-lookup"><span data-stu-id="17df2-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="17df2-139">Возвращает MAPI_TOP_LEVEL, если не были установлены флаги с помощью метода **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="17df2-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17df2-140">См. также</span><span class="sxs-lookup"><span data-stu-id="17df2-140">See also</span></span>



[<span data-ttu-id="17df2-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="17df2-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="17df2-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17df2-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="17df2-143">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="17df2-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="17df2-144">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="17df2-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="17df2-145">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="17df2-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

