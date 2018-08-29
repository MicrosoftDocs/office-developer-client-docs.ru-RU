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
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587826"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="1a80c-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="1a80c-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="1a80c-104">**Сфера применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a80c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a80c-105">Возвращает минимальное значение в методе [IMAPIProgress::SetLimits](imapiprogress-setlimits.md), для которого отображается информация о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="1a80c-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="1a80c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a80c-106">Parameters</span></span>

 <span data-ttu-id="1a80c-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="1a80c-107">_lpulMin_</span></span>
  
> <span data-ttu-id="1a80c-108">Указатель на минимальное количество элементов в операции [выходные данные].</span><span class="sxs-lookup"><span data-stu-id="1a80c-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a80c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a80c-109">Return value</span></span>

<span data-ttu-id="1a80c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a80c-110">S_OK</span></span> 
  
> <span data-ttu-id="1a80c-111">Получено минимальное количество элементов в операции.</span><span class="sxs-lookup"><span data-stu-id="1a80c-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a80c-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a80c-112">Remarks</span></span>

<span data-ttu-id="1a80c-113">Минимальное значение представляет начало операции в числовой форме.</span><span class="sxs-lookup"><span data-stu-id="1a80c-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="1a80c-114">Оно может быть глобальным максимальным значением, представляющим отображаемые данные всего хода выполнения, или локальным значением, представляющим только часть отображаемых данных.</span><span class="sxs-lookup"><span data-stu-id="1a80c-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="1a80c-115">Значение параметра флага определяет, как объект хода выполнения реагирует на минимальное значение (как на локальное или как на глобальное).</span><span class="sxs-lookup"><span data-stu-id="1a80c-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="1a80c-116">Когда флаг MAPI_TOP_LEVEL задан, минимальное значение обрабатывается как глобальное и используется для определения хода выполнения всей операции.</span><span class="sxs-lookup"><span data-stu-id="1a80c-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="1a80c-117">Когда флаг MAPI_TOP_LEVEL не задан, минимальное значение обрабатывается как локальное и поставщики используют его внутренним способом для отображения хода выполнения касательно подчиненных объектов нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="1a80c-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="1a80c-118">Объекты хода выполнения сохраняют локальное минимальное значение, только чтобы возвратить его поставщику при вызове **GetMin**.</span><span class="sxs-lookup"><span data-stu-id="1a80c-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1a80c-119">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="1a80c-119">Notes to implementers</span></span>

<span data-ttu-id="1a80c-120">Инициализируйте минимальное значение, указав 1.</span><span class="sxs-lookup"><span data-stu-id="1a80c-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="1a80c-121">Поставщики службы могут сбросить это значение путем вызова метода **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="1a80c-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="1a80c-122">Дополнительные сведения о том, как реализовать **GetMin** и другие методы [IMAPIProgress](imapiprogressiunknown.md), см. в статье [Реализация индикатора хода выполнения](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1a80c-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="1a80c-123">Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1a80c-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1a80c-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1a80c-124">MFCMAPI Reference</span></span>

<span data-ttu-id="1a80c-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1a80c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1a80c-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1a80c-126">**File**</span></span>|<span data-ttu-id="1a80c-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1a80c-127">**Function**</span></span>|<span data-ttu-id="1a80c-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1a80c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a80c-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="1a80c-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="1a80c-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="1a80c-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="1a80c-131">MFCMAPI использует метод **IMAPIProgress::GetMin**, чтобы получить минимальное значение для индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1a80c-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="1a80c-132">Возвращает 1, если ранее не были заданы ограничения путем вызова метода **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="1a80c-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a80c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1a80c-133">See also</span></span>



[<span data-ttu-id="1a80c-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="1a80c-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="1a80c-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="1a80c-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="1a80c-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="1a80c-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="1a80c-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a80c-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="1a80c-138">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="1a80c-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1a80c-139">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="1a80c-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="1a80c-140">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="1a80c-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

