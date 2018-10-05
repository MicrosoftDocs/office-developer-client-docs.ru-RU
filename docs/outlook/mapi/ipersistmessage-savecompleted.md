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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395058"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="b9a39-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="b9a39-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="b9a39-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9a39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9a39-105">Уведомляет формы, которая сохранения завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b9a39-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="b9a39-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9a39-106">Parameters</span></span>

<span data-ttu-id="b9a39-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="b9a39-107">_pMessage_</span></span>
  
> <span data-ttu-id="b9a39-108">[in] Указатель на только что сохраненный сообщения.</span><span class="sxs-lookup"><span data-stu-id="b9a39-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9a39-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9a39-109">Return value</span></span>

<span data-ttu-id="b9a39-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9a39-110">S_OK</span></span> 
  
> <span data-ttu-id="b9a39-111">Уведомление успешно.</span><span class="sxs-lookup"><span data-stu-id="b9a39-111">The notification was successful.</span></span>
    
<span data-ttu-id="b9a39-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b9a39-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="b9a39-113">Параметр _pMessage_ имеет значение NULL и форма находится в состоянии [HandsOffFromNormal](handsofffromnormal-state.md) или [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="b9a39-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="b9a39-114">ЗНАЧЕНИЕ E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="b9a39-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="b9a39-115">Форма не является одним из следующих состояний:</span><span class="sxs-lookup"><span data-stu-id="b9a39-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="b9a39-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="b9a39-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="b9a39-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="b9a39-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="b9a39-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="b9a39-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="b9a39-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9a39-119">Remarks</span></span>

<span data-ttu-id="b9a39-120">Метод **IPersistMessage::SaveCompleted** вызывается средством просмотра формы для уведомления формы, в которой были сохранены все ожидающие изменения.</span><span class="sxs-lookup"><span data-stu-id="b9a39-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="b9a39-121">**SaveCompleted** должны вызывать только в том случае, когда форма находится в одном из следующих состояний:</span><span class="sxs-lookup"><span data-stu-id="b9a39-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="b9a39-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="b9a39-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="b9a39-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="b9a39-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="b9a39-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="b9a39-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="b9a39-125">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="b9a39-125">Notes to implementers</span></span>

<span data-ttu-id="b9a39-126">Существует несколько возможных действий, которые могут выполнять метод **SaveCompleted** , в зависимости от того, какие сообщения содержит параметр-указатель и состояния сообщение находится в.</span><span class="sxs-lookup"><span data-stu-id="b9a39-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="b9a39-127">Тем не менее при успешной действие, которое всегда сохраните текущее состояние сообщения, параметр _pMessage_ и переход на новые формы в состояние [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="b9a39-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="b9a39-128">В следующей таблице описываются условия, которые влияют на действия, которые необходимо выполнять в реализации **SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="b9a39-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="b9a39-129">**Условие**</span><span class="sxs-lookup"><span data-stu-id="b9a39-129">**Condition**</span></span>|<span data-ttu-id="b9a39-130">**Действие**</span><span class="sxs-lookup"><span data-stu-id="b9a39-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9a39-131">Параметр _pMessage_ имеет значение NULL, и параметр _fSameAsLoad_ метода [IPersistMessage::Save](ipersistmessage-save.md) задано значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="b9a39-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="b9a39-132">Вызовите метод [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) всем зарегистрированным пользователям, пометить форму как чистая, а возвращаемое значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b9a39-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b9a39-133">Параметр _pMessage_ имеет значение NULL, и параметр _fSameAsLoad_ метода **IPersistMessage::Save** задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="b9a39-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="b9a39-134">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b9a39-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b9a39-135">Форма находится в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="b9a39-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="b9a39-136">Освобождение сообщения, текущий и замените указывает параметр _pMessage_ сообщение.</span><span class="sxs-lookup"><span data-stu-id="b9a39-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="b9a39-137">Вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) замены сообщения и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b9a39-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b9a39-138">Форма находится в состоянии HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="b9a39-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="b9a39-139">Вызовите метод **IMAPIViewAdviseSink::OnSaved** всем зарегистрированным пользователям, пометить форму как чистая, а возвращаемое значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b9a39-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b9a39-140">Форма находится в состоянии [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="b9a39-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="b9a39-141">Освобождение сообщения, текущий и замените сообщение, которое указывает _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="b9a39-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="b9a39-142">Вызов метода **IUnknown::AddRef** замены сообщения.</span><span class="sxs-lookup"><span data-stu-id="b9a39-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="b9a39-143">Вызовите метод **IMAPIViewAdviseSink::OnSaved** всем зарегистрированным пользователям, пометить форму как чистая, а возвращаемое значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b9a39-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="b9a39-144">Форма находится в одном из состояний HandsOff и параметр _pMessage_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b9a39-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="b9a39-145">Возвращает E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="b9a39-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="b9a39-146">Форма находится в состоянии от одного из состояний HandsOff или NoScribble.</span><span class="sxs-lookup"><span data-stu-id="b9a39-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="b9a39-147">Возвращает значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="b9a39-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="b9a39-148">Дополнительные сведения о сохранении объектов хранилища [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) или [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) методов см.</span><span class="sxs-lookup"><span data-stu-id="b9a39-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9a39-149">См. также</span><span class="sxs-lookup"><span data-stu-id="b9a39-149">See also</span></span>

- [<span data-ttu-id="b9a39-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9a39-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="b9a39-151">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="b9a39-151">Form States</span></span>](form-states.md)
