---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9ea44c9ba75390f06ff12ddeed0c7b652538e07d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808915"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="1a01c-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="1a01c-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="1a01c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a01c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a01c-105">Запросы, формы выполнить все задачи связывается с определенным команды.</span><span class="sxs-lookup"><span data-stu-id="1a01c-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="1a01c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a01c-106">Parameters</span></span>

 <span data-ttu-id="1a01c-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="1a01c-107">_iVerb_</span></span>
  
> <span data-ttu-id="1a01c-108">[in] Номер, связанный с одной из команд формы.</span><span class="sxs-lookup"><span data-stu-id="1a01c-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="1a01c-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="1a01c-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="1a01c-110">[in] Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="1a01c-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="1a01c-111">Параметр _lpViewContext_ может иметь **значение null**.</span><span class="sxs-lookup"><span data-stu-id="1a01c-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="1a01c-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="1a01c-112">_hwndParent_</span></span>
  
> <span data-ttu-id="1a01c-113">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="1a01c-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="1a01c-114">Значение параметра _hwndParent_ должно быть **значение null,** Если диалоговое окно или окно не является модальным.</span><span class="sxs-lookup"><span data-stu-id="1a01c-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="1a01c-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="1a01c-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="1a01c-116">[in] Указатель на объект Win32 структуры [Прямоугольник](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) , содержащий размер и положение окна формы.</span><span class="sxs-lookup"><span data-stu-id="1a01c-116">[in] A pointer to a Win32 [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1a01c-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1a01c-117">Return value</span></span>

<span data-ttu-id="1a01c-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1a01c-118">S_OK</span></span> 
  
> <span data-ttu-id="1a01c-119">Команда успешно вызова.</span><span class="sxs-lookup"><span data-stu-id="1a01c-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="1a01c-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="1a01c-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="1a01c-121">Команда, представленное параметром _iVerb_ является допустимым, но формы не могут выполнять операции, связанные с ним в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="1a01c-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1a01c-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a01c-122">Remarks</span></span>

<span data-ttu-id="1a01c-123">Средства просмотра форм вызовите метод **IMAPIForm::DoVerb** для запроса, что форма выполнения задач, связывается с каждой командой, которая поддерживает формы.</span><span class="sxs-lookup"><span data-stu-id="1a01c-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="1a01c-124">Числовое значение, переданной в **DoVerb** с помощью параметра _iVerb_ отмечаются каждого из поддерживаемых команд.</span><span class="sxs-lookup"><span data-stu-id="1a01c-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="1a01c-125">Типичная реализация **DoVerb** содержат операторе **switch** для проверки значения, подходящие для параметра _iVerb_ для формы.</span><span class="sxs-lookup"><span data-stu-id="1a01c-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1a01c-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1a01c-126">Notes to implementers</span></span>

<span data-ttu-id="1a01c-127">Если средство просмотра формы с помощью параметра _lpViewContext_ указывает контекст представления, используйте его в реализации **DoVerb** вместо контекст представления, переданные в более ранних вызова метода [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="1a01c-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="1a01c-128">Внесите необходимые изменения, необходимые для вашего внутренних структур данных и не следует сохранять контекст представления.</span><span class="sxs-lookup"><span data-stu-id="1a01c-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="1a01c-129">В реализации **DoVerb** выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="1a01c-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="1a01c-130">Выполнение код не требуется для конкретной команды, который связан с параметром _iVerb_ .</span><span class="sxs-lookup"><span data-stu-id="1a01c-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="1a01c-131">При необходимости восстановите исходное контекст представления.</span><span class="sxs-lookup"><span data-stu-id="1a01c-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="1a01c-132">Если был передан на номер Неизвестный команды, возвратите MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="1a01c-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="1a01c-133">В противном случае возвращает результат на основании успешное или неудачное выполнены необходимые команды.</span><span class="sxs-lookup"><span data-stu-id="1a01c-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="1a01c-134">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="1a01c-134">Close the form.</span></span> <span data-ttu-id="1a01c-135">Отвечает всегда для закрытия формы после завершения вызова **DoVerb** .</span><span class="sxs-lookup"><span data-stu-id="1a01c-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="1a01c-136">Некоторые действия, такие как печать, должны быть модальными по отношению к **DoVerb** звонок, то есть, указанный операция должна быть выполнена до возвращения вызова **DoVerb** .</span><span class="sxs-lookup"><span data-stu-id="1a01c-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="1a01c-137">Для получения структуры **Прямоугольник** , используемых окно формы, вызовите функцию [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="1a01c-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="1a01c-138">Не сохранять дескриптор в параметре _hwndParent_ , потому что несмотря на то, что обычно действует до завершения **DoVerb**, его можно удалять сразу же после возврата звонка.</span><span class="sxs-lookup"><span data-stu-id="1a01c-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1a01c-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1a01c-139">Notes to callers</span></span>

<span data-ttu-id="1a01c-140">Можно выполнять команды немодальную выступать в качестве модальные окна команд, указав _lpViewContext_ для реализации контекст представления, которое возвращает флаг VCSTATUS_MODAL из метода [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="1a01c-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="1a01c-141">Дополнительные сведения о команд в MAPI можно [Команд формы](form-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="1a01c-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="1a01c-142">Дополнительные сведения об обработке команд в OLE можно [OLE и передачи данных](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a01c-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1a01c-143">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="1a01c-143">MFCMAPI reference</span></span>

<span data-ttu-id="1a01c-144">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="1a01c-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1a01c-145">**����**</span><span class="sxs-lookup"><span data-stu-id="1a01c-145">**File**</span></span>|<span data-ttu-id="1a01c-146">**�������**</span><span class="sxs-lookup"><span data-stu-id="1a01c-146">**Function**</span></span>|<span data-ttu-id="1a01c-147">**�����������**</span><span class="sxs-lookup"><span data-stu-id="1a01c-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a01c-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="1a01c-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1a01c-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="1a01c-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="1a01c-150">Mfcmapi (en) использует метод **IMAPIForm::DoVerb** для вызова команды на форме.</span><span class="sxs-lookup"><span data-stu-id="1a01c-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a01c-151">См. также</span><span class="sxs-lookup"><span data-stu-id="1a01c-151">See also</span></span>



[<span data-ttu-id="1a01c-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="1a01c-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="1a01c-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="1a01c-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="1a01c-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a01c-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="1a01c-155">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1a01c-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1a01c-156">Команды форм</span><span class="sxs-lookup"><span data-stu-id="1a01c-156">Form Verbs</span></span>](form-verbs.md)

