---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317131"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="67c13-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="67c13-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="67c13-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67c13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67c13-105">Загружает форму для указанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="67c13-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="67c13-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="67c13-106">Parameters</span></span>

 <span data-ttu-id="67c13-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="67c13-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="67c13-108">[in] Указатель на сайт сообщения для загрузки формы.</span><span class="sxs-lookup"><span data-stu-id="67c13-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="67c13-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="67c13-109">_pMessage_</span></span>
  
> <span data-ttu-id="67c13-110">[in] Указатель на сообщение, для которого должна быть загружена форма.</span><span class="sxs-lookup"><span data-stu-id="67c13-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="67c13-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="67c13-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="67c13-112">[in] Битмаска флагов, определенных клиентом или поставщика, скопированная  из свойства PR_MSG_STATUS сообщения[(PidTagMessageStatus),](pidtagmessagestatus-canonical-property.md)которые предоставляют сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="67c13-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="67c13-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="67c13-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="67c13-114">[in] Битмашка флагов, скопированная из свойства[PR_MESSAGE_FLAGS (PidTagMessageFlags),](pidtagmessageflags-canonical-property.md)которые предоставляют дополнительные сведения о состоянии сообщения. </span><span class="sxs-lookup"><span data-stu-id="67c13-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67c13-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67c13-115">Return value</span></span>

<span data-ttu-id="67c13-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="67c13-116">S_OK</span></span> 
  
> <span data-ttu-id="67c13-117">Форма была успешно загружена.</span><span class="sxs-lookup"><span data-stu-id="67c13-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67c13-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="67c13-118">Remarks</span></span>

<span data-ttu-id="67c13-119">Зрители форм называют **метод IPersistMessage::Load** для загрузки формы для существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="67c13-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="67c13-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="67c13-120">Notes to implementers</span></span>

 <span data-ttu-id="67c13-121">**Нагрузка** вызвана только в том случае, если форма находится в одном из следующих штатов:</span><span class="sxs-lookup"><span data-stu-id="67c13-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="67c13-122">Uninitialized</span><span class="sxs-lookup"><span data-stu-id="67c13-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="67c13-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="67c13-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="67c13-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="67c13-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="67c13-125">Если зритель формы вызывает **Load,** пока форма находится в любом другом состоянии, метод возвращается E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="67c13-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="67c13-126">Если ваша форма имеет ссылку на активный сайт сообщений, который не передается в **Load,** отпустите исходный сайт, так как он больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="67c13-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="67c13-127">Храните указатели на сайте сообщений и сообщения из параметров  _pMessageSite_ и  _pMessage_ и вызывайте методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) для приумношения их отсчетов ссылок.</span><span class="sxs-lookup"><span data-stu-id="67c13-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="67c13-128">После **завершения AddRef** храните свойства  _ulMessageStatus_ и  _ulMessageFlags_ в форму.</span><span class="sxs-lookup"><span data-stu-id="67c13-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="67c13-129">Перед ее отображением перенаправляем форму в нормальное состояние и уведомляем зарегистрированных зрителей, вызывая их методы [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md) [](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="67c13-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="67c13-130">Если ошибки не происходят, S_OK.</span><span class="sxs-lookup"><span data-stu-id="67c13-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67c13-131">См. также</span><span class="sxs-lookup"><span data-stu-id="67c13-131">See also</span></span>



[<span data-ttu-id="67c13-132">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="67c13-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="67c13-133">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="67c13-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="67c13-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67c13-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="67c13-135">Единое состояние</span><span class="sxs-lookup"><span data-stu-id="67c13-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="67c13-136">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="67c13-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="67c13-137">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="67c13-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="67c13-138">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="67c13-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="67c13-139">IPersistStorage::Load</span><span class="sxs-lookup"><span data-stu-id="67c13-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="67c13-140">IPersistStream::Load</span><span class="sxs-lookup"><span data-stu-id="67c13-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="67c13-141">IPersistFile::Load</span><span class="sxs-lookup"><span data-stu-id="67c13-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

