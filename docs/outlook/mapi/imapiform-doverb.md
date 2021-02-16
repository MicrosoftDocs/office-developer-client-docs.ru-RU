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
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329463"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="2733f-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="2733f-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="2733f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2733f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2733f-105">Запрашивает выполнение формы любых задач, которые она связывает с определенной глаголом.</span><span class="sxs-lookup"><span data-stu-id="2733f-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="2733f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2733f-106">Parameters</span></span>

 <span data-ttu-id="2733f-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="2733f-107">_iVerb_</span></span>
  
> <span data-ttu-id="2733f-108">[in] Номер, связанный с одной из глаголов формы.</span><span class="sxs-lookup"><span data-stu-id="2733f-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="2733f-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="2733f-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="2733f-110">[in] Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="2733f-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="2733f-111">Параметр _lpViewContext_ может иметь **null.**</span><span class="sxs-lookup"><span data-stu-id="2733f-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="2733f-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="2733f-112">_hwndParent_</span></span>
  
> <span data-ttu-id="2733f-113">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span><span class="sxs-lookup"><span data-stu-id="2733f-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="2733f-114">Параметр  _hwndParent должен_ иметь **null,** если диалоговое окно или окно не является модальным.</span><span class="sxs-lookup"><span data-stu-id="2733f-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="2733f-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="2733f-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="2733f-116">[in] Указатель на структуру [Win32 RECT,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) содержаную размер и положение окна формы.</span><span class="sxs-lookup"><span data-stu-id="2733f-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2733f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2733f-117">Return value</span></span>

<span data-ttu-id="2733f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2733f-118">S_OK</span></span> 
  
> <span data-ttu-id="2733f-119">Глагол успешно вызван.</span><span class="sxs-lookup"><span data-stu-id="2733f-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="2733f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="2733f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="2733f-121">Глагол, представленный параметром  _iVerb,_ действителен, но форма не может выполнять связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="2733f-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2733f-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="2733f-122">Remarks</span></span>

<span data-ttu-id="2733f-123">Посетители форм звонят **методу IMAPIForm::D oVerb,** чтобы запрашивать выполнение формы задач, которые она связывает с каждым глаголом, поддерживаемым формой.</span><span class="sxs-lookup"><span data-stu-id="2733f-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="2733f-124">Каждая из поддерживаемых глаголов определена числом, переданным **в DoVerb** в _параметре iVerb._</span><span class="sxs-lookup"><span data-stu-id="2733f-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="2733f-125">Типичные реализации **DoVerb содержат** коммутатор, который проверяет значения, допустимые для  _параметра iVerb_ для формы.</span><span class="sxs-lookup"><span data-stu-id="2733f-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2733f-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2733f-126">Notes to implementers</span></span>

<span data-ttu-id="2733f-127">Если просмотр формы указывает контекст представления в параметре _lpViewContext,_ используйте его в реализации **DoVerb** вместо контекста представления, переданного в более ранних вызовах метода [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md)</span><span class="sxs-lookup"><span data-stu-id="2733f-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="2733f-128">Внести все необходимые изменения во внутренние структуры данных и не сохранять контекст представления.</span><span class="sxs-lookup"><span data-stu-id="2733f-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="2733f-129">Выполните следующие задачи в реализации **DoVerb:**</span><span class="sxs-lookup"><span data-stu-id="2733f-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="2733f-130">Выполните любой код, необходимый для конкретной команды, связанной с параметром _iVerb._</span><span class="sxs-lookup"><span data-stu-id="2733f-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="2733f-131">При необходимости восстановим исходный контекст представления.</span><span class="sxs-lookup"><span data-stu-id="2733f-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="2733f-132">Если передан неизвестный номер команды, вернетесь MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="2733f-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="2733f-133">В противном случае возвращается результат на основе успешности или сбоя выполненной команды.</span><span class="sxs-lookup"><span data-stu-id="2733f-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="2733f-134">Закроем форму.</span><span class="sxs-lookup"><span data-stu-id="2733f-134">Close the form.</span></span> <span data-ttu-id="2733f-135">Вы всегда несете ответственность за то, чтобы закрыть форму после завершения вызова **DoVerb.**</span><span class="sxs-lookup"><span data-stu-id="2733f-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="2733f-136">Некоторые команды, например Print, должны быть модальными по отношению к вызову **DoVerb,** то есть указанная операция должна быть завершена до возврата вызова **DoVerb.**</span><span class="sxs-lookup"><span data-stu-id="2733f-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="2733f-137">Чтобы получить **структуру RECT,** используемую окном формы, вызовите [функцию GetWindowRect.](https://msdn.microsoft.com/library/ms633519)</span><span class="sxs-lookup"><span data-stu-id="2733f-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="2733f-138">Не следует сохранять окне в параметре  _hwndParent,_ так как, хотя он обычно остается действительным до завершения **doVerb,** он может быть уничтожен сразу после возврата вызова.</span><span class="sxs-lookup"><span data-stu-id="2733f-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2733f-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2733f-139">Notes to callers</span></span>

<span data-ttu-id="2733f-140">Вы можете сделать так, чтобы не модальные команды выступают в качестве модальных глаголов, указав _lpViewContext_ на реализацию контекста представления, которая возвращает флаг VCSTATUS_MODAL из метода [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md)</span><span class="sxs-lookup"><span data-stu-id="2733f-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="2733f-141">Дополнительные сведения о глаголах в MAPI [см. в поддоменах Form Verbs.](form-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="2733f-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="2733f-142">Дополнительные сведения об обработке глаголов в OLE см. в [OLE и передаче данных.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2733f-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2733f-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2733f-143">MFCMAPI reference</span></span>

<span data-ttu-id="2733f-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2733f-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2733f-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="2733f-145">**File**</span></span>|<span data-ttu-id="2733f-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="2733f-146">**Function**</span></span>|<span data-ttu-id="2733f-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2733f-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2733f-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="2733f-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="2733f-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="2733f-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="2733f-150">MFCMAPI использует метод **IMAPIForm::D oVerb** для вызова команды в форме.</span><span class="sxs-lookup"><span data-stu-id="2733f-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2733f-151">См. также</span><span class="sxs-lookup"><span data-stu-id="2733f-151">See also</span></span>



[<span data-ttu-id="2733f-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="2733f-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="2733f-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="2733f-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="2733f-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2733f-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="2733f-155">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="2733f-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="2733f-156">Команды формы</span><span class="sxs-lookup"><span data-stu-id="2733f-156">Form Verbs</span></span>](form-verbs.md)

