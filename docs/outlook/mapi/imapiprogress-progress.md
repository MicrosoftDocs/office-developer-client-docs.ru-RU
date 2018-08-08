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
ms.openlocfilehash: 2a003be35fc9c3ef8efc7c66997ee99f6e578f09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809017"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="f4272-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="f4272-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="f4272-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4272-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4272-105">Обновляет индикатор хода выполнения с отображением хода выполнения после внесения до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="f4272-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="f4272-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4272-106">Parameters</span></span>

 <span data-ttu-id="f4272-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="f4272-107">_ulValue_</span></span>
  
> <span data-ttu-id="f4272-108">[in] Число, указывающее текущий уровень хода выполнения (вычисляется из параметров _инициализирует метод ulCount_ и _ulTotal_ или _lpulMin_ и _lpulMax_ параметра метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) ) между глобальное нижний предел и глобальные верхний предел.</span><span class="sxs-lookup"><span data-stu-id="f4272-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="f4272-109">_Инициализирует метод ulCount_</span><span class="sxs-lookup"><span data-stu-id="f4272-109">_ulCount_</span></span>
  
> <span data-ttu-id="f4272-110">[in] Число, указывающее в настоящее время обработанные элемента относительно итога.</span><span class="sxs-lookup"><span data-stu-id="f4272-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="f4272-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="f4272-111">_ulTotal_</span></span>
  
> <span data-ttu-id="f4272-112">[in] Общее число элементов, обрабатываемых во время операции.</span><span class="sxs-lookup"><span data-stu-id="f4272-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4272-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f4272-113">Return value</span></span>

<span data-ttu-id="f4272-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f4272-114">S_OK</span></span> 
  
> <span data-ttu-id="f4272-115">Индикатор хода выполнения обновлен успешно.</span><span class="sxs-lookup"><span data-stu-id="f4272-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="f4272-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f4272-116">Notes to implementers</span></span>

<span data-ttu-id="f4272-117">Параметр _ulValue_ будет совпадать для глобального минимальное значение только в начале операции и глобальные максимальное значение только после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="f4272-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="f4272-118">Используйте параметры _инициализирует метод ulCount_ и _ulTotal_ , если он доступен для отображения сообщения необязательно, такие как «завершено из десяти 5 элементы.»</span><span class="sxs-lookup"><span data-stu-id="f4272-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="f4272-119">Если _инициализирует метод ulCount_ и _ulTotal_ значение 0, принятие решения о изменяется индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f4272-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="f4272-120">Некоторые поставщики услуг этих параметров значение 0, чтобы указать, что они обрабатываются вложенные объекты, ход выполнения отслеживается относительно родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="f4272-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="f4272-121">В этом случае это имеет смысл, чтобы изменить способ отображения только в том случае, если родительский объект отчетов о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="f4272-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="f4272-122">Некоторые поставщики услуг передайте 0 для этих параметров каждый раз.</span><span class="sxs-lookup"><span data-stu-id="f4272-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="f4272-123">Дополнительные сведения о том, как реализовать **хода выполнения** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.</span><span class="sxs-lookup"><span data-stu-id="f4272-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f4272-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f4272-124">Notes to callers</span></span>

<span data-ttu-id="f4272-125">Не все три параметры, **IMAPIProgress::Progress** не требуется.</span><span class="sxs-lookup"><span data-stu-id="f4272-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="f4272-126">Единственный параметр, который требуется — _ulValue_, число, указывающее процент выполнения.</span><span class="sxs-lookup"><span data-stu-id="f4272-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="f4272-127">Если значение флага MAPI_TOP_LEVEL, можно также передать число объектов и всего по объекту.</span><span class="sxs-lookup"><span data-stu-id="f4272-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="f4272-128">Некоторые реализации использовать эти значения для отображения фразы, например «5 элементов завершен из десяти» с индикатором хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f4272-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="f4272-129">Если необходимо скопировать все сообщения в одной папке, необходимо задайте _ulTotal_ с общим количеством сообщения от копирования.</span><span class="sxs-lookup"><span data-stu-id="f4272-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="f4272-130">При копировании папки значение _ulTotal_ количество вложенных папок в папке.</span><span class="sxs-lookup"><span data-stu-id="f4272-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="f4272-131">Если папки для копирования содержит не вложенные папки и только сообщения, необходимо задайте _ulTotal_ значение 1.</span><span class="sxs-lookup"><span data-stu-id="f4272-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="f4272-132">Дополнительные сведения о том, как и когда следует выполнять вызовы объект о ходе выполнения в разделе [отображаемое индикатор хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="f4272-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f4272-133">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="f4272-133">MFCMAPI reference</span></span>

<span data-ttu-id="f4272-134">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="f4272-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f4272-135">**����**</span><span class="sxs-lookup"><span data-stu-id="f4272-135">**File**</span></span>|<span data-ttu-id="f4272-136">**�������**</span><span class="sxs-lookup"><span data-stu-id="f4272-136">**Function**</span></span>|<span data-ttu-id="f4272-137">**�����������**</span><span class="sxs-lookup"><span data-stu-id="f4272-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4272-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="f4272-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="f4272-139">CMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="f4272-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="f4272-140">Mfcmapi (en) использует метод **IMAPIProgress::Progress** для обновления в строке состояния mfcmapi (en) с текущей процент, вычисляемых из _uValue_ и текущей максимальное и минимальное значения.</span><span class="sxs-lookup"><span data-stu-id="f4272-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4272-141">См. также</span><span class="sxs-lookup"><span data-stu-id="f4272-141">See also</span></span>



[<span data-ttu-id="f4272-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="f4272-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="f4272-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4272-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="f4272-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f4272-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f4272-145">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="f4272-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="f4272-146">Реализация индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="f4272-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

