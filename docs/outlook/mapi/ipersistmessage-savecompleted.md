---
title: иперсистмессажесавекомплетед
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
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="3294d-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="3294d-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="3294d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3294d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3294d-105">Уведомляет форму о завершении операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="3294d-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="3294d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3294d-106">Parameters</span></span>

<span data-ttu-id="3294d-107">_пмессаже_</span><span class="sxs-lookup"><span data-stu-id="3294d-107">_pMessage_</span></span>
  
> <span data-ttu-id="3294d-108">возврата Указатель на вновь сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="3294d-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3294d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3294d-109">Return value</span></span>

<span data-ttu-id="3294d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3294d-110">S_OK</span></span> 
  
> <span data-ttu-id="3294d-111">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="3294d-111">The notification was successful.</span></span>
    
<span data-ttu-id="3294d-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3294d-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="3294d-113">Параметр _пмессаже_ имеет значение null, а форма находится в состоянии [HandsOffFromNormal](handsofffromnormal-state.md) или [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="3294d-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="3294d-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="3294d-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="3294d-115">Форма находится не в одном из следующих состояний:</span><span class="sxs-lookup"><span data-stu-id="3294d-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="3294d-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3294d-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="3294d-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="3294d-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="3294d-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="3294d-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="3294d-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="3294d-119">Remarks</span></span>

<span data-ttu-id="3294d-120">Средство просмотра форм вызывает метод **иперсистмессаже:: савекомплетед** , чтобы уведомить форму о том, что все ожидающие изменения сохранены.</span><span class="sxs-lookup"><span data-stu-id="3294d-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="3294d-121">**Савекомплетед** следует вызывать только в том случае, если форма находится в одном из следующих состояний:</span><span class="sxs-lookup"><span data-stu-id="3294d-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="3294d-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3294d-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="3294d-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="3294d-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="3294d-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="3294d-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="3294d-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3294d-125">Notes to implementers</span></span>

<span data-ttu-id="3294d-126">Существует несколько возможных действий, которые может выполнить метод **савекомплетед** в зависимости от того, что содержит параметр указателя сообщения, и в каком состоянии находится сообщение.</span><span class="sxs-lookup"><span data-stu-id="3294d-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="3294d-127">Однако при успешном выполнении действия всегда сохраняйте текущее состояние сообщения, на которое указывает параметр _пмессаже_ , и переводит форму в [нормальное](normal-state.md) состояние.</span><span class="sxs-lookup"><span data-stu-id="3294d-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="3294d-128">В следующей таблице описаны условия, которые влияют на действия, которые необходимо выполнить в реализации **савекомплетед**.</span><span class="sxs-lookup"><span data-stu-id="3294d-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="3294d-129">**Условие**</span><span class="sxs-lookup"><span data-stu-id="3294d-129">**Condition**</span></span>|<span data-ttu-id="3294d-130">**Действие**</span><span class="sxs-lookup"><span data-stu-id="3294d-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3294d-131">Параметр _пмессаже_ имеет значение null, а параметр _Фсамеаслоад_ метода " [иперсистмессаже:: Save](ipersistmessage-save.md) " имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="3294d-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="3294d-132">Вызовите метод [имапивиевадвисесинк:: OnSave](imapiviewadvisesink-onsaved.md) для всех зарегистрированных средств просмотра, помечайте форму как чистую и возвращая S_OK.</span><span class="sxs-lookup"><span data-stu-id="3294d-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3294d-133">Параметр _пмессаже_ имеет значение null, а параметр _Фсамеаслоад_ метода " **иперсистмессаже:: Save** " имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="3294d-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="3294d-134">Возврат S_OK.</span><span class="sxs-lookup"><span data-stu-id="3294d-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3294d-135">Форма находится в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="3294d-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="3294d-136">Освободите текущее сообщение и замените его сообщением, на которое указывает параметр _пмессаже_ .</span><span class="sxs-lookup"><span data-stu-id="3294d-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="3294d-137">Вызовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) сообщения rereplacement и возвратите S_OK.</span><span class="sxs-lookup"><span data-stu-id="3294d-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3294d-138">Форма находится в состоянии HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="3294d-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="3294d-139">Вызовите метод **имапивиевадвисесинк:: OnSave** для всех зарегистрированных средств просмотра, помечайте форму как чистую и возвращая S_OK.</span><span class="sxs-lookup"><span data-stu-id="3294d-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3294d-140">Форма находится в состоянии " [каракули](noscribble-state.md) ".</span><span class="sxs-lookup"><span data-stu-id="3294d-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="3294d-141">Освободите текущее сообщение и замените его сообщением, на которое указывает _пмессаже_.</span><span class="sxs-lookup"><span data-stu-id="3294d-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="3294d-142">Вызовите метод **IUnknown:: AddRef** для замещающего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3294d-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="3294d-143">Вызовите метод **имапивиевадвисесинк:: OnSave** для всех зарегистрированных средств просмотра, помечайте форму как чистую и возвращая S_OK.</span><span class="sxs-lookup"><span data-stu-id="3294d-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3294d-144">Форма находится в одном из состояний Хандсофф, а параметру _пмессаже_ ЗАДАНО значение null.</span><span class="sxs-lookup"><span data-stu-id="3294d-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="3294d-145">Возврат E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="3294d-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="3294d-146">Форма находится в состоянии, отличном от одного из состояний Хандсофф или в режиме "каракули".</span><span class="sxs-lookup"><span data-stu-id="3294d-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="3294d-147">Возврат E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="3294d-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="3294d-148">Для получения дополнительных сведений о сохранении объектов хранилища обратитесь к документации по методам [иперсистстораже:: савекомплетед](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) или [IPersistFile:: савекомплетед](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) .</span><span class="sxs-lookup"><span data-stu-id="3294d-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3294d-149">См. также</span><span class="sxs-lookup"><span data-stu-id="3294d-149">See also</span></span>

- [<span data-ttu-id="3294d-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3294d-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="3294d-151">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="3294d-151">Form States</span></span>](form-states.md)
