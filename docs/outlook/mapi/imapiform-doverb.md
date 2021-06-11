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
# <a name="imapiformdoverb"></a><span data-ttu-id="3aed2-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="3aed2-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="3aed2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3aed2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3aed2-105">Запрашивает, чтобы форма выполняла любые задачи, которые она связывает с определенным глаголом.</span><span class="sxs-lookup"><span data-stu-id="3aed2-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="3aed2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3aed2-106">Parameters</span></span>

 <span data-ttu-id="3aed2-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="3aed2-107">_iVerb_</span></span>
  
> <span data-ttu-id="3aed2-108">[in] Число, связанное с одним из глаголов формы.</span><span class="sxs-lookup"><span data-stu-id="3aed2-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="3aed2-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="3aed2-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="3aed2-110">[in] Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="3aed2-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="3aed2-111">Параметр  _lpViewContext может_ быть **null**.</span><span class="sxs-lookup"><span data-stu-id="3aed2-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="3aed2-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="3aed2-112">_hwndParent_</span></span>
  
> <span data-ttu-id="3aed2-113">[in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом.</span><span class="sxs-lookup"><span data-stu-id="3aed2-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="3aed2-114">Параметр  _hwndParent должен_ быть **null,** если диалоговое окно или окно не являются модальными.</span><span class="sxs-lookup"><span data-stu-id="3aed2-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="3aed2-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="3aed2-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="3aed2-116">[in] Указатель на структуру [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32, которая содержит размер и положение окна формы.</span><span class="sxs-lookup"><span data-stu-id="3aed2-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3aed2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3aed2-117">Return value</span></span>

<span data-ttu-id="3aed2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3aed2-118">S_OK</span></span> 
  
> <span data-ttu-id="3aed2-119">Глагол успешно вызывался.</span><span class="sxs-lookup"><span data-stu-id="3aed2-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="3aed2-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="3aed2-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="3aed2-121">Глагол, представленный  _параметром iVerb,_ действителен, но форма не может выполнять операции, связанные с ним в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="3aed2-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3aed2-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="3aed2-122">Remarks</span></span>

<span data-ttu-id="3aed2-123">Зрители формы звонят по **методу IMAPIForm::D oVerb,** чтобы запросить, чтобы форма выполняла задачи, которые она связывает с каждым глаголом, поддерживаемым формой.</span><span class="sxs-lookup"><span data-stu-id="3aed2-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="3aed2-124">Каждый из поддерживаемых глаголов идентифицирован по числовому значению, передается **в DoVerb** в _параметре iVerb._</span><span class="sxs-lookup"><span data-stu-id="3aed2-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="3aed2-125">Типичные реализации **DoVerb содержат** заявление **коммутатора,** которое проверяет значения, допустимые для  _параметра iVerb_ для формы.</span><span class="sxs-lookup"><span data-stu-id="3aed2-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3aed2-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3aed2-126">Notes to implementers</span></span>

<span data-ttu-id="3aed2-127">Если зритель формы указывает контекст представления в параметре _lpViewContext,_ используйте его в реализации **DoVerb** вместо контекста представления, переданного в предыдущий вызов методу [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md)</span><span class="sxs-lookup"><span data-stu-id="3aed2-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="3aed2-128">Внести все необходимые изменения в внутренние структуры данных и не сохранять контекст представления.</span><span class="sxs-lookup"><span data-stu-id="3aed2-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="3aed2-129">Выполните следующие задачи в реализации **DoVerb:**</span><span class="sxs-lookup"><span data-stu-id="3aed2-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="3aed2-130">Выполните любой код, необходимый для определенного глагола, связанного с параметром _iVerb._</span><span class="sxs-lookup"><span data-stu-id="3aed2-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="3aed2-131">При необходимости восстановим исходный контекст представления.</span><span class="sxs-lookup"><span data-stu-id="3aed2-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="3aed2-132">Если неизвестный номер глагола был передан, верни MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="3aed2-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="3aed2-133">В противном случае возвращаем результат, основанный на успешности или сбое любого выполненного глагола.</span><span class="sxs-lookup"><span data-stu-id="3aed2-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="3aed2-134">Закрой форму.</span><span class="sxs-lookup"><span data-stu-id="3aed2-134">Close the form.</span></span> <span data-ttu-id="3aed2-135">После завершения вызова **DoVerb** вы всегда несете ответственность за закрытие формы.</span><span class="sxs-lookup"><span data-stu-id="3aed2-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="3aed2-136">Некоторые глаголы, например Print, должны быть модальными в отношении вызова **DoVerb,** то есть указанная операция должна быть завершена до возвращения вызова **DoVerb.**</span><span class="sxs-lookup"><span data-stu-id="3aed2-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="3aed2-137">Чтобы получить **структуру RECT,** используемую в окне формы, позвоните в [функцию GetWindowRect.](https://msdn.microsoft.com/library/ms633519)</span><span class="sxs-lookup"><span data-stu-id="3aed2-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="3aed2-138">Не сохраните ручку в параметре  _hwndParent,_ так как, хотя она обычно остается допустимой до завершения **DoVerb,** она может быть уничтожена сразу после возвращения вызова.</span><span class="sxs-lookup"><span data-stu-id="3aed2-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3aed2-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3aed2-139">Notes to callers</span></span>

<span data-ttu-id="3aed2-140">Можно заставить немодальные глаголы выступать в качестве модальных глаголов, указав _lpViewContext_ на реализацию контекста представления, которая возвращает флаг VCSTATUS_MODAL из метода [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md)</span><span class="sxs-lookup"><span data-stu-id="3aed2-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="3aed2-141">Дополнительные сведения о глаголах в MAPI см. в [виде глаголов.](form-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="3aed2-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="3aed2-142">Дополнительные сведения о том, как обрабатываются глаголы в OLE, см. в [OLE и Передаче данных.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3aed2-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3aed2-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3aed2-143">MFCMAPI reference</span></span>

<span data-ttu-id="3aed2-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3aed2-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3aed2-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3aed2-145">**File**</span></span>|<span data-ttu-id="3aed2-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3aed2-146">**Function**</span></span>|<span data-ttu-id="3aed2-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3aed2-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3aed2-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="3aed2-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="3aed2-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="3aed2-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="3aed2-150">MFCMAPI использует **метод IMAPIForm::D oVerb** для вызова глагола в форме.</span><span class="sxs-lookup"><span data-stu-id="3aed2-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3aed2-151">См. также</span><span class="sxs-lookup"><span data-stu-id="3aed2-151">See also</span></span>



[<span data-ttu-id="3aed2-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="3aed2-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="3aed2-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="3aed2-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="3aed2-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3aed2-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="3aed2-155">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="3aed2-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="3aed2-156">Глаголы формы</span><span class="sxs-lookup"><span data-stu-id="3aed2-156">Form Verbs</span></span>](form-verbs.md)

