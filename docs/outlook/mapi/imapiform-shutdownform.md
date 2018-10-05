---
title: IMAPIFormShutdownForm
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384838"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="dc8d2-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="dc8d2-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="dc8d2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc8d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc8d2-105">Закрывает форму.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="dc8d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc8d2-106">Parameters</span></span>

 <span data-ttu-id="dc8d2-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="dc8d2-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="dc8d2-108">[in] Значение, определяющее, как или ли данные в форме сохраняется до закрытия формы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="dc8d2-109">Можно установить один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="dc8d2-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="dc8d2-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="dc8d2-111">Не следует сохранить данные формы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="dc8d2-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="dc8d2-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="dc8d2-113">Пользователь должен запрос на сохранение любых измененных данных в форме.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="dc8d2-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="dc8d2-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="dc8d2-115">Необходимо сохранить данные формы, если он был изменен с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="dc8d2-116">Если пользовательский интерфейс не отображается, формы при необходимости можно переключиться на использование функциональные возможности для параметра SAVEOPTS_NOSAVE.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc8d2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc8d2-117">Return value</span></span>

<span data-ttu-id="dc8d2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc8d2-118">S_OK</span></span> 
  
> <span data-ttu-id="dc8d2-119">Форма была закрыта.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-119">The form was closed.</span></span>
    
<span data-ttu-id="dc8d2-120">ЗНАЧЕНИЕ E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="dc8d2-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="dc8d2-121">Форма уже была закрыта во время предыдущего вызова **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc8d2-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc8d2-122">Remarks</span></span>

<span data-ttu-id="dc8d2-123">Средства просмотра форм вызовите метод **IMAPIForm::ShutdownForm** для закрытия формы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dc8d2-124">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="dc8d2-124">Notes to implementers</span></span>

<span data-ttu-id="dc8d2-125">В реализации **ShutdownForm**выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="dc8d2-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="dc8d2-126">Проверьте, что средство просмотра еще не звонил **ShutdownForm**и возвратить значение E_UNEXPECTED, если она есть.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="dc8d2-127">Хотя это маловероятно, следует проверить.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="dc8d2-128">Вызов метода [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) формы, чтобы хранилища, используемого в форме и все внутренние структуры данных доступны только после завершения обработки.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="dc8d2-129">Определите, есть ли несохраненные изменения к данным формы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="dc8d2-130">Сохраните несохраненные данные в соответствии с как задать параметр _ulSaveOptions_ путем вызова метода [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="dc8d2-131">Уничтожает окно интерфейса пользователя формы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="dc8d2-132">Освобождение сообщения и объекты сайта сообщение формы, вызвав их [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) методы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="dc8d2-133">Сообщить все зарегистрированные пользователи, просматривающие ожидание завершения работы, вызвав их [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) методы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="dc8d2-134">Вызовите метод [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) для отмены регистрации формы для уведомлений, задав указателя приемника уведомлений значение **null**.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="dc8d2-135">Вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить память для свойств формы.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="dc8d2-136">Вызовите метод **функции IUnknown::Release** формы, соответствующие **AddRef** вызов, выполненный на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="dc8d2-137">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="dc8d2-138">После выполнения этих действий допустимо только методы объекта формы, который может вызывать — это списки из интерфейс [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dc8d2-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc8d2-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dc8d2-139">Notes to callers</span></span>

<span data-ttu-id="dc8d2-140">При возврате **ShutdownForm** , независимо от того, является ли он возвращает ошибку, release формы путем вызова метода **функции IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="dc8d2-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="dc8d2-141">Можно игнорировать любые ошибки, возвращаемые **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="dc8d2-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc8d2-142">См. также</span><span class="sxs-lookup"><span data-stu-id="dc8d2-142">See also</span></span>



[<span data-ttu-id="dc8d2-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="dc8d2-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="dc8d2-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="dc8d2-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="dc8d2-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="dc8d2-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="dc8d2-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dc8d2-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dc8d2-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc8d2-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

