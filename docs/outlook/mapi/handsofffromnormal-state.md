---
title: Состояние HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808585"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="caf44-103">Состояние HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="caf44-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="caf44-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="caf44-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="caf44-105">Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="caf44-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="caf44-106">Он является частью процесс сохранения содержимое формы в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="caf44-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="caf44-107">При работе в это состояние означает, объекта формы следует отказаться от внесения изменений в памяти копии значений свойств сообщений, так как не может быть другой возможности, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="caf44-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="caf44-108">В следующей таблице описываются допустимые переходы из состояния HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="caf44-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="caf44-109">IPersistMessage ** метод **</span><span class="sxs-lookup"><span data-stu-id="caf44-109">****IPersistMessage** method**</span></span>|<span data-ttu-id="caf44-110">**Действие**</span><span class="sxs-lookup"><span data-stu-id="caf44-110">**Action**</span></span>|<span data-ttu-id="caf44-111">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="caf44-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="caf44-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ значение NULL)</span><span class="sxs-lookup"><span data-stu-id="caf44-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="caf44-113">Замените объект message сообщение _pMessage_которого является заменой отозван предыдущего вызова [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)сообщение.</span><span class="sxs-lookup"><span data-stu-id="caf44-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="caf44-114">Данные в новое сообщение гарантированно такой же, как отозванного сообщения.</span><span class="sxs-lookup"><span data-stu-id="caf44-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="caf44-115">Сообщение не должен быть помечен как чистая, а также [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) вызван после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="caf44-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="caf44-116">Если выполнен вызов **SaveCompleted** введите состояние [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="caf44-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="caf44-117">В противном случае остаются в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="caf44-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="caf44-118">Обычный или HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="caf44-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="caf44-119">**IPersistMessage::SaveCompleted** (_pMessage ==_ значение NULL)</span><span class="sxs-lookup"><span data-stu-id="caf44-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="caf44-120">Присвоено значение E_UNEXPECTED последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="caf44-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="caf44-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="caf44-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="caf44-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)или [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="caf44-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="caf44-123">Присвоено значение E_UNEXPECTED последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="caf44-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="caf44-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="caf44-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="caf44-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="caf44-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="caf44-126">Возвращает последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="caf44-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="caf44-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="caf44-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="caf44-128">Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="caf44-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="caf44-129">Присвоено значение E_UNEXPECTED последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="caf44-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="caf44-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="caf44-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="caf44-131">См. также</span><span class="sxs-lookup"><span data-stu-id="caf44-131">See also</span></span>



[<span data-ttu-id="caf44-132">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="caf44-132">Form States</span></span>](form-states.md)

