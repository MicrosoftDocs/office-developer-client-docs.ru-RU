---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317138"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="8fca0-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="8fca0-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="8fca0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fca0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fca0-105">Сообщает форму о том, что операция сохранения завершена.</span><span class="sxs-lookup"><span data-stu-id="8fca0-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="8fca0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8fca0-106">Parameters</span></span>

<span data-ttu-id="8fca0-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="8fca0-107">_pMessage_</span></span>
  
> <span data-ttu-id="8fca0-108">[in] Указатель на недавно сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="8fca0-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8fca0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fca0-109">Return value</span></span>

<span data-ttu-id="8fca0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fca0-110">S_OK</span></span> 
  
> <span data-ttu-id="8fca0-111">Уведомление было успешным.</span><span class="sxs-lookup"><span data-stu-id="8fca0-111">The notification was successful.</span></span>
    
<span data-ttu-id="8fca0-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8fca0-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="8fca0-113">Параметр _pMessage_ — NULL, а форма находится в состоянии [HandsOffFromNormal](handsofffromnormal-state.md) или [HandsOffAfterSave.](handsoffaftersave-state.md)</span><span class="sxs-lookup"><span data-stu-id="8fca0-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="8fca0-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="8fca0-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="8fca0-115">Форма не находится в одном из следующих штатов:</span><span class="sxs-lookup"><span data-stu-id="8fca0-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="8fca0-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="8fca0-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="8fca0-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8fca0-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="8fca0-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="8fca0-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="8fca0-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="8fca0-119">Remarks</span></span>

<span data-ttu-id="8fca0-120">Метод **IPersistMessage::SaveCompleted** вызван просмотром форм, чтобы уведомить форму о том, что все ожидающих изменений сохранены.</span><span class="sxs-lookup"><span data-stu-id="8fca0-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="8fca0-121">**SaveCompleted** следует называть только в том случае, если форма находится в одном из следующих штатов:</span><span class="sxs-lookup"><span data-stu-id="8fca0-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="8fca0-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="8fca0-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="8fca0-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8fca0-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="8fca0-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="8fca0-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="8fca0-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8fca0-125">Notes to implementers</span></span>

<span data-ttu-id="8fca0-126">Существует несколько возможных действий, которые может выполнять метод **SaveCompleted,** в зависимости от того, что содержит параметр указателя сообщения и в каком состоянии находится сообщение.</span><span class="sxs-lookup"><span data-stu-id="8fca0-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="8fca0-127">Однако при успешном действии всегда сохраните текущее состояние сообщения, на которое указывает параметр  _pMessage,_ и перенаправляем форму в [нормальное](normal-state.md) состояние.</span><span class="sxs-lookup"><span data-stu-id="8fca0-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="8fca0-128">В следующей таблице описываются условия, влияющие на действия, которые необходимо принять при реализации **SaveCompleted.**</span><span class="sxs-lookup"><span data-stu-id="8fca0-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="8fca0-129">**Условие**</span><span class="sxs-lookup"><span data-stu-id="8fca0-129">**Condition**</span></span>|<span data-ttu-id="8fca0-130">**Действие**</span><span class="sxs-lookup"><span data-stu-id="8fca0-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fca0-131">Параметр  _pMessage_ — NULL, а  _параметр fSameAsLoad_ метода [IPersistMessage::Сохранить](ipersistmessage-save.md) задан для TRUE.</span><span class="sxs-lookup"><span data-stu-id="8fca0-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="8fca0-132">Вызовите [метод IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) для всех зарегистрированных зрителей, пометить форму как чистую и S_OK.</span><span class="sxs-lookup"><span data-stu-id="8fca0-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="8fca0-133">Параметр  _pMessage_ — NULL, а  _параметр fSameAsLoad_ метода **IPersistMessage::Сохранить** задан для FALSE.</span><span class="sxs-lookup"><span data-stu-id="8fca0-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="8fca0-134">Возвращение S_OK.</span><span class="sxs-lookup"><span data-stu-id="8fca0-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="8fca0-135">Форма находится в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="8fca0-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="8fca0-136">Освободите текущее сообщение и замените его сообщением, на которое указывает параметр _pMessage._</span><span class="sxs-lookup"><span data-stu-id="8fca0-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="8fca0-137">Вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) и S_OK.</span><span class="sxs-lookup"><span data-stu-id="8fca0-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="8fca0-138">Форма находится в состоянии HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="8fca0-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="8fca0-139">Вызовите **метод IMAPIViewAdviseSink::OnSaved** для всех зарегистрированных зрителей, пометить форму как чистую и S_OK.</span><span class="sxs-lookup"><span data-stu-id="8fca0-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="8fca0-140">Форма находится в состоянии [NoScribble.](noscribble-state.md)</span><span class="sxs-lookup"><span data-stu-id="8fca0-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="8fca0-141">Освободите текущее сообщение и замените его сообщением, на которое указывает _pMessage._</span><span class="sxs-lookup"><span data-stu-id="8fca0-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="8fca0-142">Вызов метода **IUnknown::AddRef** сообщения замены.</span><span class="sxs-lookup"><span data-stu-id="8fca0-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="8fca0-143">Вызовите **метод IMAPIViewAdviseSink::OnSaved** для всех зарегистрированных зрителей, пометить форму как чистую и S_OK.</span><span class="sxs-lookup"><span data-stu-id="8fca0-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="8fca0-144">Форма находится в одном из состояниях HandsOff, а параметр  _pMessage_ задан в NULL.</span><span class="sxs-lookup"><span data-stu-id="8fca0-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="8fca0-145">Возвращение E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8fca0-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="8fca0-146">Форма находится в состоянии, помимо одного из состояния HandsOff или состояния NoScribble.</span><span class="sxs-lookup"><span data-stu-id="8fca0-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="8fca0-147">Возвращение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8fca0-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="8fca0-148">Дополнительные сведения о сохранении объектов хранения см. в документации по методам [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) или [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted)</span><span class="sxs-lookup"><span data-stu-id="8fca0-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fca0-149">См. также</span><span class="sxs-lookup"><span data-stu-id="8fca0-149">See also</span></span>

- [<span data-ttu-id="8fca0-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8fca0-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="8fca0-151">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="8fca0-151">Form States</span></span>](form-states.md)
