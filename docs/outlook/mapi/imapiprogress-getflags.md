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
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423645"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="77528-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="77528-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="77528-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77528-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77528-105">Возвращает параметры флага из объекта progress для уровня операции, на котором рассчитывается информация о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="77528-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="77528-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77528-106">Parameters</span></span>

 <span data-ttu-id="77528-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="77528-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="77528-108">[out] Битоваяmas флагов, которая управляет уровнем операции, на котором рассчитывается информация о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="77528-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="77528-109">Можно вернуть следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="77528-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="77528-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="77528-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="77528-111">Ход выполнения рассчитывается для объекта верхнего уровня, который вызван клиентом для начала операции.</span><span class="sxs-lookup"><span data-stu-id="77528-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="77528-112">Например, объектом верхнего уровня в операции копирования папок является папка, которая копируется.</span><span class="sxs-lookup"><span data-stu-id="77528-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="77528-113">Если MAPI_TOP_LEVEL не установлен, ход выполнения вычисляется для объекта нижнего уровня или подобекта.</span><span class="sxs-lookup"><span data-stu-id="77528-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="77528-114">В операции копирования папок объект нижнего уровня — это одна из вложенных папок в копируется папке.</span><span class="sxs-lookup"><span data-stu-id="77528-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77528-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77528-115">Return value</span></span>

<span data-ttu-id="77528-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="77528-116">S_OK</span></span> 
  
> <span data-ttu-id="77528-117">Значение флагов было возвращено успешно.</span><span class="sxs-lookup"><span data-stu-id="77528-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77528-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="77528-118">Remarks</span></span>

<span data-ttu-id="77528-119">MAPI позволяет поставщикам услуг различать объекты верхнего уровня и подобъекты с помощью флага MAPI_TOP_LEVEL, чтобы все объекты, участвующие в операции, могли использовать ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для демонстрации хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="77528-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="77528-120">Это приводит к плавному переходу индикатора в одном положительном направлении.</span><span class="sxs-lookup"><span data-stu-id="77528-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="77528-121">Установлен ли MAPI_TOP_LEVEL определяет, как поставщики служб устанавливают другие параметры в последующих вызовах к объекту хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="77528-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="77528-122">Значение, возвращаемого **getFlags,** сначала устанавливается поставщиком услуг с помощью вызова метода [IMAPIProgress::SetLimits.](imapiprogress-setlimits.md)</span><span class="sxs-lookup"><span data-stu-id="77528-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="77528-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="77528-123">Notes to implementers</span></span>

<span data-ttu-id="77528-124">Всегда инициализировать флаг для MAPI_TOP_LEVEL, а затем по необходимости с его очисткой полагайтесь на поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="77528-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="77528-125">Поставщики услуг могут очистить и сбросить флаг, вызывая метод **IMAPIProgress::SetLimits.**</span><span class="sxs-lookup"><span data-stu-id="77528-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="77528-126">Дополнительные сведения о реализации **GetFlags** и других методов **IMAPIProgress** см. в подразделе ["Реализация индикатора хода выполнения".](implementing-a-progress-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="77528-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="77528-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="77528-127">Notes to callers</span></span>

<span data-ttu-id="77528-128">При отображии индикатора хода выполнения сначала вызовите **IMAPIProgress::GetFlags.**</span><span class="sxs-lookup"><span data-stu-id="77528-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="77528-129">Возвращаемому значению следует MAPI_TOP_LEVEL, так как все реализации инициализируют содержимое параметра  _lpulFlags_ до этого значения.</span><span class="sxs-lookup"><span data-stu-id="77528-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="77528-130">Дополнительные сведения о последовательности вызовов объекта хода выполнения см. в этой [теме.](how-to-display-a-progress-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="77528-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="77528-131">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="77528-131">MFCMAPI reference</span></span>

<span data-ttu-id="77528-132">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="77528-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="77528-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="77528-133">**File**</span></span>|<span data-ttu-id="77528-134">**Функция**</span><span class="sxs-lookup"><span data-stu-id="77528-134">**Function**</span></span>|<span data-ttu-id="77528-135">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="77528-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77528-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="77528-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="77528-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="77528-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="77528-138">MFCMAPI использует метод **IMAPIProgress::GetFlags** для определения установленных флагов.</span><span class="sxs-lookup"><span data-stu-id="77528-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="77528-139">Возвращает MAPI_TOP_LEVEL если флаги не были установлены с помощью метода **IMAPIProgress::SetLimits.**</span><span class="sxs-lookup"><span data-stu-id="77528-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77528-140">См. также</span><span class="sxs-lookup"><span data-stu-id="77528-140">See also</span></span>



[<span data-ttu-id="77528-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="77528-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="77528-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77528-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="77528-143">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="77528-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="77528-144">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="77528-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="77528-145">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="77528-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

