---
title: имапипрогрессжетфлагс
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
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423645"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="7b23d-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="7b23d-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="7b23d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b23d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b23d-105">Возвращает параметры флага из объекта Progress для уровня операции, на котором рассчитываются сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="7b23d-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7b23d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b23d-106">Parameters</span></span>

 <span data-ttu-id="7b23d-107">_лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="7b23d-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="7b23d-108">вышли Битовая маска флагов, которые управляют уровнем работы, на котором рассчитываются сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="7b23d-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="7b23d-109">Можно вернуть следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7b23d-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="7b23d-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="7b23d-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="7b23d-111">Выполняется вычисление хода выполнения для объекта верхнего уровня, объекта, вызываемого клиентом для начала операции.</span><span class="sxs-lookup"><span data-stu-id="7b23d-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="7b23d-112">Например, объект верхнего уровня в операции копирования папки — это копируемая папка.</span><span class="sxs-lookup"><span data-stu-id="7b23d-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="7b23d-113">Если MAPI_TOP_LEVEL не задано, выполняется вычисление хода выполнения для объекта нижнего уровня или подобъекта.</span><span class="sxs-lookup"><span data-stu-id="7b23d-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="7b23d-114">В операции копирования папки объект нижнего уровня является одной из вложенных папок в копируемой папке.</span><span class="sxs-lookup"><span data-stu-id="7b23d-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b23d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b23d-115">Return value</span></span>

<span data-ttu-id="7b23d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b23d-116">S_OK</span></span> 
  
> <span data-ttu-id="7b23d-117">Значение флагов успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="7b23d-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b23d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b23d-118">Remarks</span></span>

<span data-ttu-id="7b23d-119">MAPI позволяет поставщикам услуг различать объекты верхнего уровня и подобъекты с помощью флага MAPI_TOP_LEVEL, чтобы все объекты, участвующие в операции, могли использовать одну и ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для отображения хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7b23d-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="7b23d-120">Это приводит к плавному отображению индикатора в отдельном положительном направлении.</span><span class="sxs-lookup"><span data-stu-id="7b23d-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="7b23d-121">Установлен ли флаг MAPI_TOP_LEVEL определяет, как поставщики услуг устанавливают другие параметры при последующих вызовах объекта Progress.</span><span class="sxs-lookup"><span data-stu-id="7b23d-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="7b23d-122">Значение, возвращаемое методом "- **flags** ", изначально задается средством реализации, а затем поставщиком услуг при вызове метода [IMAPIProgress:: SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="7b23d-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7b23d-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7b23d-123">Notes to implementers</span></span>

<span data-ttu-id="7b23d-124">Всегда инициализируйте флаг, чтобы он MAPI_TOP_LEVEL, а затем полагается на поставщиков услуг, чтобы при необходимости его очистить.</span><span class="sxs-lookup"><span data-stu-id="7b23d-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="7b23d-125">Поставщики услуг могут очистить и сбросить флаг, вызвав метод **IMAPIProgress:: SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="7b23d-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="7b23d-126">Дополнительные сведения о том, как реализовать **Флаги** и другие методы **IMAPIProgress** , приведены в разделе [Реализация индикатора хода выполнения](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="7b23d-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b23d-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7b23d-127">Notes to callers</span></span>

<span data-ttu-id="7b23d-128">При отображении индикатора хода выполнения первым вызывается вызов **IMAPIProgress:: @ flags**.</span><span class="sxs-lookup"><span data-stu-id="7b23d-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="7b23d-129">Возвращаемое значение должно быть MAPI_TOP_LEVEL, так как все реализации инициализируют содержимое параметра _лпулфлагс_ значением.</span><span class="sxs-lookup"><span data-stu-id="7b23d-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="7b23d-130">Дополнительные сведения о последовательности вызовов для объекта Progress приведены в разделе [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="7b23d-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b23d-131">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7b23d-131">MFCMAPI reference</span></span>

<span data-ttu-id="7b23d-132">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7b23d-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b23d-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7b23d-133">**File**</span></span>|<span data-ttu-id="7b23d-134">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7b23d-134">**Function**</span></span>|<span data-ttu-id="7b23d-135">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7b23d-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b23d-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="7b23d-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="7b23d-137">Кмапипрогресс:: @ flags</span><span class="sxs-lookup"><span data-stu-id="7b23d-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="7b23d-138">MFCMAPI использует метод **IMAPIProgress::** ' для определения устанавливаемых флагов.</span><span class="sxs-lookup"><span data-stu-id="7b23d-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="7b23d-139">Возвращает MAPI_TOP_LEVEL, если флаги не заданы с помощью метода **IMAPIProgress:: SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="7b23d-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b23d-140">См. также</span><span class="sxs-lookup"><span data-stu-id="7b23d-140">See also</span></span>



[<span data-ttu-id="7b23d-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="7b23d-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="7b23d-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b23d-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="7b23d-143">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="7b23d-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7b23d-144">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="7b23d-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="7b23d-145">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="7b23d-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

