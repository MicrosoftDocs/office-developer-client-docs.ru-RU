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
# <a name="imapiprogressgetflags"></a><span data-ttu-id="6899d-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="6899d-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="6899d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6899d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6899d-105">Возвращает флаг, параметры из объекта о ходе выполнения для уровня операции, на котором рассчитывается сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="6899d-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6899d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6899d-106">Parameters</span></span>

 <span data-ttu-id="6899d-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="6899d-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="6899d-108">[out] Битовая маска флаги, определяющее уровень операции, на какие хода выполнения рассчитывается сведения.</span><span class="sxs-lookup"><span data-stu-id="6899d-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="6899d-109">Может быть возвращено следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6899d-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="6899d-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="6899d-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="6899d-111">Ход выполнения рассчитывается для объекта верхнего уровня, объект, который будет вызываться клиентом для начала операции.</span><span class="sxs-lookup"><span data-stu-id="6899d-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="6899d-112">Например объект верхнего уровня в операцию копирования папки — это папка, которое выполняется копирование.</span><span class="sxs-lookup"><span data-stu-id="6899d-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="6899d-113">Если MAPI_TOP_LEVEL не задано, о ходе выполнения рассчитывается для нижнего уровня объекта или вложенные объекты.</span><span class="sxs-lookup"><span data-stu-id="6899d-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="6899d-114">В операцию копирования папки нижнего уровня объекта является одним из вложенных папок в папке, в которое выполняется копирование.</span><span class="sxs-lookup"><span data-stu-id="6899d-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6899d-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6899d-115">Return value</span></span>

<span data-ttu-id="6899d-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6899d-116">S_OK</span></span> 
  
> <span data-ttu-id="6899d-117">Успешно возвращено значение флаги.</span><span class="sxs-lookup"><span data-stu-id="6899d-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6899d-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="6899d-118">Remarks</span></span>

<span data-ttu-id="6899d-119">MAPI поставщики услуг для различения объектов верхнего уровня и вложенных с флагом MAPI_TOP_LEVEL, чтобы все объекты задействованных в рамках одной операции можно использовать ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для отображения хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6899d-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="6899d-120">В этом случае отображения индикатора осуществляются без проблем в одном направлении положительное.</span><span class="sxs-lookup"><span data-stu-id="6899d-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="6899d-121">Установлен ли флаг MAPI_TOP_LEVEL определяет, как поставщиков услуг задавать другие параметры в последующие запросы к объекту хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6899d-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="6899d-122">Изначально принимает значение, возвращенное **GetFlags** средством реализации, а затем поставщиком услуг путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="6899d-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6899d-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="6899d-123">Notes to implementers</span></span>

<span data-ttu-id="6899d-124">Всегда инициализировать флаг, MAPI_TOP_LEVEL и затем использовать поставщиков услуг, снимите его в случае необходимости.</span><span class="sxs-lookup"><span data-stu-id="6899d-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="6899d-125">Поставщиков услуг можно очистить и Сбросить флаг путем вызова метода **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="6899d-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="6899d-126">Дополнительные сведения о том, как реализовать **GetFlags** и другие методы **IMAPIProgress** [Индикатор выполнения](implementing-a-progress-indicator.md)см.</span><span class="sxs-lookup"><span data-stu-id="6899d-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="6899d-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6899d-127">Notes to callers</span></span>

<span data-ttu-id="6899d-128">При отображении индикатор выполнения вызова первого звонка с **IMAPIProgress::GetFlags**.</span><span class="sxs-lookup"><span data-stu-id="6899d-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="6899d-129">Возвращаемое значение должно быть MAPI_TOP_LEVEL, так как все реализации инициализировать содержимое параметр _lpulFlags_ это значение.</span><span class="sxs-lookup"><span data-stu-id="6899d-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="6899d-130">Дополнительные сведения о последовательности вызовов объекта хода выполнения просмотрите [представление индикатор хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="6899d-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6899d-131">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="6899d-131">MFCMAPI reference</span></span>

<span data-ttu-id="6899d-132">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="6899d-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6899d-133">**����**</span><span class="sxs-lookup"><span data-stu-id="6899d-133">**File**</span></span>|<span data-ttu-id="6899d-134">**�������**</span><span class="sxs-lookup"><span data-stu-id="6899d-134">**Function**</span></span>|<span data-ttu-id="6899d-135">**�����������**</span><span class="sxs-lookup"><span data-stu-id="6899d-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6899d-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="6899d-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="6899d-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="6899d-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="6899d-138">Mfcmapi (en) использует метод **IMAPIProgress::GetFlags** , чтобы определить, какие флаги установлены.</span><span class="sxs-lookup"><span data-stu-id="6899d-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="6899d-139">Возвращает MAPI_TOP_LEVEL, если не были установлены флаги с помощью метода **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="6899d-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6899d-140">См. также</span><span class="sxs-lookup"><span data-stu-id="6899d-140">See also</span></span>



[<span data-ttu-id="6899d-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="6899d-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="6899d-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6899d-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="6899d-143">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6899d-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6899d-144">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="6899d-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="6899d-145">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="6899d-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

