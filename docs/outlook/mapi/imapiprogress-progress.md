---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435497"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="c296c-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="c296c-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="c296c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c296c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c296c-105">Обновляет индикатор прогресса с отображением прогресса по мере выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c296c-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="c296c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c296c-106">Parameters</span></span>

 <span data-ttu-id="c296c-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="c296c-107">_ulValue_</span></span>
  
> <span data-ttu-id="c296c-108">[in] Число, которое указывает текущий уровень прогресса (вычисляется из _параметров ulCount_ и _ulTotal_ или _lpulMin и lpulMax_ метода [IMAPIProgress::SetLimits)](imapiprogress-setlimits.md) между глобальным нижним пределом и глобальным верхним пределом. </span><span class="sxs-lookup"><span data-stu-id="c296c-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="c296c-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="c296c-109">_ulCount_</span></span>
  
> <span data-ttu-id="c296c-110">[in] Число, которое указывает обработанный в настоящее время элемент относительно общего числа.</span><span class="sxs-lookup"><span data-stu-id="c296c-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="c296c-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="c296c-111">_ulTotal_</span></span>
  
> <span data-ttu-id="c296c-112">[in] Общее количество элементов, обрабатываемых во время операции.</span><span class="sxs-lookup"><span data-stu-id="c296c-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c296c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c296c-113">Return value</span></span>

<span data-ttu-id="c296c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="c296c-114">S_OK</span></span> 
  
> <span data-ttu-id="c296c-115">Индикатор прогресса был успешно обновлен.</span><span class="sxs-lookup"><span data-stu-id="c296c-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c296c-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c296c-116">Notes to implementers</span></span>

<span data-ttu-id="c296c-117">Параметр  _ulValue_ будет равен глобальному минимальному значению только в начале операции и глобальному максимальному значению только по завершении операции.</span><span class="sxs-lookup"><span data-stu-id="c296c-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="c296c-118">Если это доступно, используйте  _параметры ulCount_ и  _ulTotal,_ чтобы отобразить необязательные сообщения, такие как "5 элементов, завершенных из 10".</span><span class="sxs-lookup"><span data-stu-id="c296c-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="c296c-119">Если  _для ulCount_ и  _ulTotal_ установлено 0, определите, следует ли визуально изменять индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="c296c-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="c296c-120">Некоторые поставщики услуг устанавливают эти параметры до 0, чтобы указать, что они обрабатывают подобект, ход которого отслеживается по отношению к родительскому объекту.</span><span class="sxs-lookup"><span data-stu-id="c296c-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="c296c-121">В этой ситуации имеет смысл изменять дисплей только после того, как родительский объект сообщает о прогрессе.</span><span class="sxs-lookup"><span data-stu-id="c296c-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="c296c-122">Некоторые поставщики услуг каждый раз передают 0 для этих параметров.</span><span class="sxs-lookup"><span data-stu-id="c296c-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="c296c-123">Дополнительные сведения о том, как реализовать **progress** и другие [](implementing-a-progress-indicator.md)методы [IMAPIProgress,](imapiprogressiunknown.md) см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="c296c-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c296c-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c296c-124">Notes to callers</span></span>

<span data-ttu-id="c296c-125">Не все три параметра **IMAPIProgress::P требуются.**</span><span class="sxs-lookup"><span data-stu-id="c296c-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="c296c-126">Единственным параметром, который требуется, является  _ulValue_, число, которое указывает процент прогресса.</span><span class="sxs-lookup"><span data-stu-id="c296c-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="c296c-127">Если задат MAPI_TOP_LEVEL, можно также передать количество объектов и общее число объектов.</span><span class="sxs-lookup"><span data-stu-id="c296c-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="c296c-128">Некоторые реализации используют эти значения для отображения фразы, например "5 элементов, завершенных из 10" с индикатором прогресса.</span><span class="sxs-lookup"><span data-stu-id="c296c-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="c296c-129">Если вы копируете все сообщения в одной папке, установите  _ulTotal_ к общему числу копируется сообщений.</span><span class="sxs-lookup"><span data-stu-id="c296c-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="c296c-130">Если вы копируете папку, установите  _ulTotal_ к числу подстановок в папке.</span><span class="sxs-lookup"><span data-stu-id="c296c-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="c296c-131">Если скопированная папка не содержит подстановок и только сообщений, установите  _ulTotal_ до 1.</span><span class="sxs-lookup"><span data-stu-id="c296c-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="c296c-132">Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="c296c-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c296c-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c296c-133">MFCMAPI reference</span></span>

<span data-ttu-id="c296c-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c296c-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c296c-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c296c-135">**File**</span></span>|<span data-ttu-id="c296c-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c296c-136">**Function**</span></span>|<span data-ttu-id="c296c-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c296c-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c296c-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="c296c-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="c296c-139">CMAPIProgress::P rogress</span><span class="sxs-lookup"><span data-stu-id="c296c-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="c296c-140">MFCMAPI использует метод **IMAPIProgress::P rogress** для обновления панели состояния MFCMAPI с текущим процентом прогресса, вычисляемого из  _uValue_ и текущих максимальных и минимальных значений.</span><span class="sxs-lookup"><span data-stu-id="c296c-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c296c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="c296c-141">See also</span></span>



[<span data-ttu-id="c296c-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="c296c-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="c296c-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c296c-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="c296c-144">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="c296c-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c296c-145">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="c296c-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="c296c-146">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="c296c-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

