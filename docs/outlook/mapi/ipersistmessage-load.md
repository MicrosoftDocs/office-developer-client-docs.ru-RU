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
ms.openlocfilehash: eff192b0d2b5cde51a2909452b19ffe1a47b2c04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809491"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="4b0b9-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="4b0b9-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="4b0b9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b0b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b0b9-105">Загружает формы для указанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4b0b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b0b9-106">Parameters</span></span>

 <span data-ttu-id="4b0b9-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="4b0b9-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="4b0b9-108">[in] Указатель на сообщение сайта для формы для загрузки.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="4b0b9-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="4b0b9-109">_pMessage_</span></span>
  
> <span data-ttu-id="4b0b9-110">[in] Указатель на сообщение, для которого следует загрузить форму.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="4b0b9-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="4b0b9-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="4b0b9-112">[in] Битовая маска флагов клиента или поставщика, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщение, предоставляют информацию о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="4b0b9-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="4b0b9-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="4b0b9-114">[in] Битовая маска флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщение, предоставляют информацию о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b0b9-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4b0b9-115">Return value</span></span>

<span data-ttu-id="4b0b9-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4b0b9-116">S_OK</span></span> 
  
> <span data-ttu-id="4b0b9-117">Форма успешно загружен.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b0b9-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b0b9-118">Remarks</span></span>

<span data-ttu-id="4b0b9-119">Средства просмотра форм вызовите метод **IPersistMessage::Load** для загрузки формы для существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4b0b9-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="4b0b9-120">Notes to implementers</span></span>

 <span data-ttu-id="4b0b9-121">**Нагрузки** вызывается только при открытии формы в одном из следующих состояний:</span><span class="sxs-lookup"><span data-stu-id="4b0b9-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="4b0b9-122">Неинициализированная переменная</span><span class="sxs-lookup"><span data-stu-id="4b0b9-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="4b0b9-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="4b0b9-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="4b0b9-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="4b0b9-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="4b0b9-125">Если форма просмотра вызывает **нагрузки** , пока форма находится в другое состояние, метод возвращает значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="4b0b9-126">Если форма имеет ссылку на сайт active сообщение помимо того, передаваемый в **нагрузки**, так как он больше не будет использоваться release исходного сайта.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="4b0b9-127">Хранение указатели на сайт сообщений и сообщений из параметров _pMessageSite_ и _pMessage_ и вызвать методы [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) оба объекта для увеличения их счетчики ссылок.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="4b0b9-128">После завершения **AddRef** хранилища свойств из параметров _ulMessageStatus_ и _ulMessageFlags_ в данный момент форму.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="4b0b9-129">Перенос форм в состояние [Normal](normal-state.md) перед их отображением и уведомить зарегистрированных средств просмотра, вызвав их [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) методы.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="4b0b9-130">При отсутствии ошибок возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="4b0b9-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b0b9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4b0b9-131">See also</span></span>



[<span data-ttu-id="4b0b9-132">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="4b0b9-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="4b0b9-133">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="4b0b9-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="4b0b9-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b0b9-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="4b0b9-135">Неинициализированное состояние</span><span class="sxs-lookup"><span data-stu-id="4b0b9-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="4b0b9-136">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="4b0b9-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="4b0b9-137">Состояние HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="4b0b9-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="4b0b9-138">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="4b0b9-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="4b0b9-139">IPersistStorage::Load</span><span class="sxs-lookup"><span data-stu-id="4b0b9-139">IPersistStorage::Load</span></span>](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="4b0b9-140">IPersistStream::Load</span><span class="sxs-lookup"><span data-stu-id="4b0b9-140">IPersistStream::Load</span></span>](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="4b0b9-141">IPersistFile::Load</span><span class="sxs-lookup"><span data-stu-id="4b0b9-141">IPersistFile::Load</span></span>](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

