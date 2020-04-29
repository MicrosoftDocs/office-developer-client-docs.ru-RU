---
title: имапиформшутдовнформ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329479"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="f71b0-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="f71b0-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="f71b0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f71b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f71b0-105">Закрывает форму.</span><span class="sxs-lookup"><span data-stu-id="f71b0-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="f71b0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f71b0-106">Parameters</span></span>

 <span data-ttu-id="f71b0-107">_улсавеоптионс_</span><span class="sxs-lookup"><span data-stu-id="f71b0-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="f71b0-108">возврата Значение, определяющее способ сохранения данных формы перед ее закрытием.</span><span class="sxs-lookup"><span data-stu-id="f71b0-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="f71b0-109">Можно задать один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="f71b0-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="f71b0-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="f71b0-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="f71b0-111">Данные формы не должны быть сохранены.</span><span class="sxs-lookup"><span data-stu-id="f71b0-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="f71b0-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="f71b0-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="f71b0-113">Пользователю должно быть предложено сохранить все измененные данные в форме.</span><span class="sxs-lookup"><span data-stu-id="f71b0-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="f71b0-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="f71b0-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="f71b0-115">Данные формы необходимо сохранить, если они были изменены с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="f71b0-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="f71b0-116">Если пользовательский интерфейс не отображается, форму можно дополнительно переключить на использование функций для параметра SAVEOPTS_NOSAVE.</span><span class="sxs-lookup"><span data-stu-id="f71b0-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f71b0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f71b0-117">Return value</span></span>

<span data-ttu-id="f71b0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f71b0-118">S_OK</span></span> 
  
> <span data-ttu-id="f71b0-119">Форма была закрыта.</span><span class="sxs-lookup"><span data-stu-id="f71b0-119">The form was closed.</span></span>
    
<span data-ttu-id="f71b0-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="f71b0-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="f71b0-121">Форма уже закрыта при предыдущем вызове **шутдовнформ**.</span><span class="sxs-lookup"><span data-stu-id="f71b0-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f71b0-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="f71b0-122">Remarks</span></span>

<span data-ttu-id="f71b0-123">Средства просмотра форм вызывают метод **имапиформ:: шутдовнформ** для закрытия формы.</span><span class="sxs-lookup"><span data-stu-id="f71b0-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f71b0-124">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f71b0-124">Notes to implementers</span></span>

<span data-ttu-id="f71b0-125">Выполните следующие задачи в реализации **шутдовнформ**:</span><span class="sxs-lookup"><span data-stu-id="f71b0-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="f71b0-126">Убедитесь, что средство просмотра еще не вызвало **шутдовнформ**, и возвращайте E_UNEXPECTED, если он есть.</span><span class="sxs-lookup"><span data-stu-id="f71b0-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="f71b0-127">Хотя это маловероятно, необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="f71b0-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="f71b0-128">Вызовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) формы, чтобы хранилище для формы и все внутренние структуры данных оставались доступными до завершения обработки.</span><span class="sxs-lookup"><span data-stu-id="f71b0-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="f71b0-129">Определите, нет ли несохраненных изменений данных формы.</span><span class="sxs-lookup"><span data-stu-id="f71b0-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="f71b0-130">Сохраните несохраненные данные в соответствии с определением параметра _улсавеоптионс_ , вызвав метод [Имапимессажесите:: савемессаже](imapimessagesite-savemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="f71b0-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="f71b0-131">Удалите окно пользовательского интерфейса формы.</span><span class="sxs-lookup"><span data-stu-id="f71b0-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="f71b0-132">Освободите объекты-сообщения и сообщения формы, вызвав их методы [выпусков IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f71b0-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="f71b0-133">Сообщите обо всех зарегистрированных средствах просмотра ожидания завершения, вызвав их методы [имапивиевадвисесинк:: OnShutdown](imapiviewadvisesink-onshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="f71b0-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="f71b0-134">Вызовите метод [имапивиевконтекст:: сетадвисесинк](imapiviewcontext-setadvisesink.md) , чтобы отменить регистрацию формы для уведомления, задав для указателя приемника уведомлений **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f71b0-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="f71b0-135">Вызовите функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить память для свойств формы.</span><span class="sxs-lookup"><span data-stu-id="f71b0-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="f71b0-136">Вызовите метод **IUnknown:: Release** формы, который соответствует вызову **AddRef** , выполненному на этапе 2.</span><span class="sxs-lookup"><span data-stu-id="f71b0-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="f71b0-137">Возврат S_OK.</span><span class="sxs-lookup"><span data-stu-id="f71b0-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f71b0-138">После выполнения этих действий единственные допустимые методы в объекте Form, которые могут быть вызваны, — это из интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f71b0-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f71b0-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f71b0-139">Notes to callers</span></span>

<span data-ttu-id="f71b0-140">Когда **шутдовнформ** возвращает значение, независимо от того, возвращает ли ошибка, освобождайте форму, вызвав ее метод **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="f71b0-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="f71b0-141">Вы можете спокойно игнорировать все ошибки, возвращенные **шутдовнформ**.</span><span class="sxs-lookup"><span data-stu-id="f71b0-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f71b0-142">См. также</span><span class="sxs-lookup"><span data-stu-id="f71b0-142">See also</span></span>



[<span data-ttu-id="f71b0-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="f71b0-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="f71b0-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="f71b0-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="f71b0-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f71b0-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="f71b0-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f71b0-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f71b0-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f71b0-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

