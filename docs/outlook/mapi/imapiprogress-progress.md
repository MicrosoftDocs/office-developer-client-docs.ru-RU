---
title: Имапипрогресспрогресс
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
# <a name="imapiprogressprogress"></a><span data-ttu-id="c3d4c-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="c3d4c-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="c3d4c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3d4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3d4c-105">Обновляет индикатор хода выполнения с отображением хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="c3d4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3d4c-106">Parameters</span></span>

 <span data-ttu-id="c3d4c-107">_Улвалуе_</span><span class="sxs-lookup"><span data-stu-id="c3d4c-107">_ulValue_</span></span>
  
> <span data-ttu-id="c3d4c-108">возврата Число, которое показывает текущий уровень выполнения (рассчитывается из параметров _улкаунт_ и _ултотал_ или из параметров _лпулмин_ и _лпулмакс_ метода [IMAPIProgress:: SetLimits](imapiprogress-setlimits.md) ) между глобальной Нижний предел и глобальное верхнее предельное значение.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="c3d4c-109">_Улкаунт_</span><span class="sxs-lookup"><span data-stu-id="c3d4c-109">_ulCount_</span></span>
  
> <span data-ttu-id="c3d4c-110">возврата Число, которое обозначает обрабатываемый в данный момент элемент относительно итогового значения.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="c3d4c-111">_Ултотал_</span><span class="sxs-lookup"><span data-stu-id="c3d4c-111">_ulTotal_</span></span>
  
> <span data-ttu-id="c3d4c-112">возврата Общее количество элементов, которые должны быть обработаны во время операции.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c3d4c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3d4c-113">Return value</span></span>

<span data-ttu-id="c3d4c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3d4c-114">S_OK</span></span> 
  
> <span data-ttu-id="c3d4c-115">Индикатор хода выполнения успешно обновлен.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c3d4c-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c3d4c-116">Notes to implementers</span></span>

<span data-ttu-id="c3d4c-117">Значение параметра _улвалуе_ будет равно глобальному минимальному значению только при запуске операции и глобальном максимальном значении только при выполнении операции.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="c3d4c-118">Используйте параметры _улкаунт_ и _ултотал_ , если они доступны, для отображения необязательного сообщения, например "5 элементов завершено из 10".</span><span class="sxs-lookup"><span data-stu-id="c3d4c-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="c3d4c-119">Если для _улкаунт_ и _ултотал_ задано значение 0, решите, следует ли визуально изменить индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="c3d4c-120">Некоторые поставщики услуг присвойте этим параметрам значение 0, чтобы указать, что они обрабатывают подобъект, ход выполнения которого отслеживается относительно родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="c3d4c-121">В этом случае имеет смысл изменить отображение только в том случае, если родительский объект сообщает о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="c3d4c-122">Некоторые поставщики услуг каждый раз каждый раз передает значение 0 для этих параметров.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="c3d4c-123">Дополнительные сведения о том, как реализовать **ход выполнения** и другие методы [IMAPIProgress](imapiprogressiunknown.md) , приведены в разделе [Реализация индикатора хода выполнения](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="c3d4c-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c3d4c-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c3d4c-124">Notes to callers</span></span>

<span data-ttu-id="c3d4c-125">Не все три параметра **IMAPIProgress: требуются:P рогресс** .</span><span class="sxs-lookup"><span data-stu-id="c3d4c-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="c3d4c-126">Единственный обязательный параметр — _улвалуе_, число, указывающее процент выполнения.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="c3d4c-127">Если установлен флаг МАПИ_ТОП_ЛЕВЕЛ, можно также передать Счетчик объектов и общий объект.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="c3d4c-128">Некоторые реализации используют эти значения для отображения фразы, например "5 элементов, завершенных из 10" с индикатором хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="c3d4c-129">Если вы копируете все сообщения в одну папку, задайте для параметра _ултотал_ общее количество копируемых сообщений.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="c3d4c-130">При копировании папки задайте для параметра _ултотал_ количество вложенных папок в папке.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="c3d4c-131">Если копируемая папка не содержит вложенных папок и сообщений, задайте для параметра _ултотал_ значение 1.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="c3d4c-132">Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="c3d4c-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c3d4c-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c3d4c-133">MFCMAPI reference</span></span>

<span data-ttu-id="c3d4c-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c3d4c-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c3d4c-135">**File**</span></span>|<span data-ttu-id="c3d4c-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c3d4c-136">**Function**</span></span>|<span data-ttu-id="c3d4c-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c3d4c-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3d4c-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="c3d4c-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="c3d4c-139">Кмапипрогресс::P рогресс</span><span class="sxs-lookup"><span data-stu-id="c3d4c-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="c3d4c-140">MFCMAPI использует метод **IMAPIProgress::P рогресс** , чтобы обновить строку состояния MFCMAPI с текущим процентом прохождения, вычисленным из _увалуе_ и текущим максимальным и минимальным значениями.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3d4c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="c3d4c-141">See also</span></span>



[<span data-ttu-id="c3d4c-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="c3d4c-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="c3d4c-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3d4c-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="c3d4c-144">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="c3d4c-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c3d4c-145">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="c3d4c-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="c3d4c-146">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="c3d4c-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

