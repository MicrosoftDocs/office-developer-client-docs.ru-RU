---
title: имапиформдоверб
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
# <a name="imapiformdoverb"></a><span data-ttu-id="197bd-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="197bd-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="197bd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="197bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="197bd-105">Запрашивает выполнение формой любых задач, которые она связывает с определенной командой.</span><span class="sxs-lookup"><span data-stu-id="197bd-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="197bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="197bd-106">Parameters</span></span>

 <span data-ttu-id="197bd-107">_иверб_</span><span class="sxs-lookup"><span data-stu-id="197bd-107">_iVerb_</span></span>
  
> <span data-ttu-id="197bd-108">возврата Число, связанное с одной из команд формы.</span><span class="sxs-lookup"><span data-stu-id="197bd-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="197bd-109">_лпвиевконтекст_</span><span class="sxs-lookup"><span data-stu-id="197bd-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="197bd-110">возврата Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="197bd-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="197bd-111">Параметр _лпвиевконтекст_ может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="197bd-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="197bd-112">_хвндпарент_</span><span class="sxs-lookup"><span data-stu-id="197bd-112">_hwndParent_</span></span>
  
> <span data-ttu-id="197bd-113">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="197bd-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="197bd-114">Параметр _хвндпарент_ должен иметь **значение NULL** , если диалоговое окно или окно не являются модальными.</span><span class="sxs-lookup"><span data-stu-id="197bd-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="197bd-115">_лпркпосрект_</span><span class="sxs-lookup"><span data-stu-id="197bd-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="197bd-116">возврата Указатель на структуру [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32, которая содержит размер и положение окна формы.</span><span class="sxs-lookup"><span data-stu-id="197bd-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="197bd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="197bd-117">Return value</span></span>

<span data-ttu-id="197bd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="197bd-118">S_OK</span></span> 
  
> <span data-ttu-id="197bd-119">Команда успешно вызвана.</span><span class="sxs-lookup"><span data-stu-id="197bd-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="197bd-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="197bd-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="197bd-121">Команда, представленная параметром _иверб_ , является допустимой, но форма не может выполнять операции, связанные с ней.</span><span class="sxs-lookup"><span data-stu-id="197bd-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="197bd-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="197bd-122">Remarks</span></span>

<span data-ttu-id="197bd-123">Средства просмотра форм вызывают метод **имапиформ::D оверб** , чтобы запросить выполнение задач, которые она связывает с каждой командой, поддерживаемой формой.</span><span class="sxs-lookup"><span data-stu-id="197bd-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="197bd-124">Каждая из поддерживаемых команд идентифицируется с помощью числового значения, которое передается в **доверб** в параметре _иверб_ .</span><span class="sxs-lookup"><span data-stu-id="197bd-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="197bd-125">Типичные реализации **доверб** содержат оператор **switch** , который проверяет значения, допустимые для параметра _иверб_ в форме.</span><span class="sxs-lookup"><span data-stu-id="197bd-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="197bd-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="197bd-126">Notes to implementers</span></span>

<span data-ttu-id="197bd-127">Если средство просмотра формы определяет контекст представления в параметре _лпвиевконтекст_ , используйте его в реализации **доверб** , а не в контексте представления, переданном при предыдущем вызове метода [имапиформ:: сетвиевконтекст](imapiform-setviewcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="197bd-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="197bd-128">Внесите все необходимые изменения во внутренние структуры данных и не сохраняйте контекст представления.</span><span class="sxs-lookup"><span data-stu-id="197bd-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="197bd-129">Выполните следующие задачи в реализации **доверб** :</span><span class="sxs-lookup"><span data-stu-id="197bd-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="197bd-130">Выполните любой код, который необходим для конкретной команды, связанной с параметром _иверб_ .</span><span class="sxs-lookup"><span data-stu-id="197bd-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="197bd-131">При необходимости восстановите исходный контекст представления.</span><span class="sxs-lookup"><span data-stu-id="197bd-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="197bd-132">Если был передан Неизвестный номер команды, возвращается MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="197bd-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="197bd-133">В противном случае возвращает результат на основе успешности или сбоя любой выполняемой команды.</span><span class="sxs-lookup"><span data-stu-id="197bd-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="197bd-134">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="197bd-134">Close the form.</span></span> <span data-ttu-id="197bd-135">Она всегда отвечает за закрытие формы после завершения вызова **доверб** .</span><span class="sxs-lookup"><span data-stu-id="197bd-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="197bd-136">Некоторые глаголы, такие как Print, должны быть модальными по отношению к вызову **доверб** — то есть перед возвратом вызова **доверб** необходимо завершить указанную операцию.</span><span class="sxs-lookup"><span data-stu-id="197bd-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="197bd-137">Чтобы получить структуру **Rect** , используемую окном формы, вызовите функцию [жетвиндоврект](https://msdn.microsoft.com/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="197bd-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="197bd-138">Не сохраняйте дескриптор в параметре _хвндпарент_ , несмотря на то, что он обычно остается действительным до завершения **доверб**, он может быть удален сразу после возврата звонка.</span><span class="sxs-lookup"><span data-stu-id="197bd-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="197bd-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="197bd-139">Notes to callers</span></span>

<span data-ttu-id="197bd-140">Немодальные команды можно сделать модальными глаголами, наведя _лпвиевконтекст_ на реализацию контекста представления, которая возвращает флаг VCSTATUS_MODAL из метода [Имапивиевконтекст:: жетвиевстатус](imapiviewcontext-getviewstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="197bd-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="197bd-141">Дополнительные сведения о командах в MAPI приведены в разделе [команды формы](form-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="197bd-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="197bd-142">Для получения дополнительных сведений о том, как команды обрабатываются в OLE, ознакомьтесь с разработкой [OLE и передачи данных](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="197bd-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="197bd-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="197bd-143">MFCMAPI reference</span></span>

<span data-ttu-id="197bd-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="197bd-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="197bd-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="197bd-145">**File**</span></span>|<span data-ttu-id="197bd-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="197bd-146">**Function**</span></span>|<span data-ttu-id="197bd-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="197bd-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="197bd-148">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="197bd-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="197bd-149">Кмимапиформвиевер:: Каллдоверб</span><span class="sxs-lookup"><span data-stu-id="197bd-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="197bd-150">MFCMAPI использует метод **имапиформ::D оверб** для вызова команды в форме.</span><span class="sxs-lookup"><span data-stu-id="197bd-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="197bd-151">См. также</span><span class="sxs-lookup"><span data-stu-id="197bd-151">See also</span></span>



[<span data-ttu-id="197bd-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="197bd-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="197bd-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="197bd-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="197bd-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="197bd-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="197bd-155">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="197bd-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="197bd-156">Команды форм</span><span class="sxs-lookup"><span data-stu-id="197bd-156">Form Verbs</span></span>](form-verbs.md)

