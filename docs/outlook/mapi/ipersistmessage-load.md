---
title: Иперсистмессажелоад
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
# <a name="ipersistmessageload"></a><span data-ttu-id="777a7-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="777a7-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="777a7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="777a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="777a7-105">ЗаГружает форму для указанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="777a7-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="777a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="777a7-106">Parameters</span></span>

 <span data-ttu-id="777a7-107">_Пмессажесите_</span><span class="sxs-lookup"><span data-stu-id="777a7-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="777a7-108">возврата Указатель на сайт сообщений для загружаемой формы.</span><span class="sxs-lookup"><span data-stu-id="777a7-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="777a7-109">_Пмессаже_</span><span class="sxs-lookup"><span data-stu-id="777a7-109">_pMessage_</span></span>
  
> <span data-ttu-id="777a7-110">возврата Указатель на сообщение, для которого должна быть загружена форма.</span><span class="sxs-lookup"><span data-stu-id="777a7-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="777a7-111">_Улмессажестатус_</span><span class="sxs-lookup"><span data-stu-id="777a7-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="777a7-112">возврата Битовая маска определяемых клиентом или поставщика флагов, скопированная из свойства **пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, которые предоставляют сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="777a7-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="777a7-113">_Улмессажефлагс_</span><span class="sxs-lookup"><span data-stu-id="777a7-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="777a7-114">возврата Битовая маска флагов, скопированных из свойства сообщения **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), которые предоставляют дополнительные сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="777a7-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="777a7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="777a7-115">Return value</span></span>

<span data-ttu-id="777a7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="777a7-116">S_OK</span></span> 
  
> <span data-ttu-id="777a7-117">Форма успешно загружена.</span><span class="sxs-lookup"><span data-stu-id="777a7-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="777a7-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="777a7-118">Remarks</span></span>

<span data-ttu-id="777a7-119">Средства просмотра форм вызывают метод **иперсистмессаже:: Load** для загрузки формы для существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="777a7-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="777a7-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="777a7-120">Notes to implementers</span></span>

 <span data-ttu-id="777a7-121">Метод **Load** вызывается только в том случае, если форма находится в одном из следующих состояний:</span><span class="sxs-lookup"><span data-stu-id="777a7-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="777a7-122">Неинициализированное</span><span class="sxs-lookup"><span data-stu-id="777a7-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="777a7-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="777a7-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="777a7-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="777a7-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="777a7-125">Если средство просмотра формы вызывает **загрузку** , когда форма находится в любом другом состоянии, метод возвращает е_унекспектед.</span><span class="sxs-lookup"><span data-stu-id="777a7-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="777a7-126">Если форма содержит ссылку на активный сайт сообщений, отличную от переданной в **загрузку**, освободите исходный сайт, так как он больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="777a7-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="777a7-127">Храните указатели на сайт сообщения и сообщение из параметров _пмессажесите_ и _пмессаже_ , а также вызывайте оба объекта: методы [AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) для увеличения счетчиков ссылок.</span><span class="sxs-lookup"><span data-stu-id="777a7-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="777a7-128">После завершения **AddRef** сохраните свойства из параметров _улмессажестатус_ и _улмессажефлагс_ в форме.</span><span class="sxs-lookup"><span data-stu-id="777a7-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="777a7-129">Перед отображением формы переведите ее в [нормальное](normal-state.md) состояние и уведомите зарегистрированных средств просмотра, вызвав их методы [Имапивиевадвисесинк:: онневмессаже](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="777a7-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="777a7-130">Если ошибок не возникло, возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="777a7-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="777a7-131">См. также</span><span class="sxs-lookup"><span data-stu-id="777a7-131">See also</span></span>



[<span data-ttu-id="777a7-132">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="777a7-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="777a7-133">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="777a7-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="777a7-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="777a7-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="777a7-135">Неинициализированное состояние</span><span class="sxs-lookup"><span data-stu-id="777a7-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="777a7-136">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="777a7-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="777a7-137">Состояние HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="777a7-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="777a7-138">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="777a7-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="777a7-139">Иперсистстораже:: Load</span><span class="sxs-lookup"><span data-stu-id="777a7-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="777a7-140">IPersistStream:: Load</span><span class="sxs-lookup"><span data-stu-id="777a7-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="777a7-141">IPersistFile:: Load</span><span class="sxs-lookup"><span data-stu-id="777a7-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

