---
title: HandsOffFromNormal State
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426473"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="a5b36-103">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="a5b36-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="a5b36-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5b36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5b36-105">Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave.](handsoffaftersave-state.md)</span><span class="sxs-lookup"><span data-stu-id="a5b36-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="a5b36-106">Это часть процесса сохранения содержимого формы в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="a5b36-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="a5b36-107">В этом состоянии объект формы должен отказаться от внесения изменений в копии значений свойств сообщения в памяти, так как может не быть другой возможности сохранить эти изменения.</span><span class="sxs-lookup"><span data-stu-id="a5b36-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="a5b36-108">В следующей таблице описаны разрешенные переходы из состояния HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="a5b36-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="a5b36-109">Метод IPersistMessage\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a5b36-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="a5b36-110">**Действие**</span><span class="sxs-lookup"><span data-stu-id="a5b36-110">**Action**</span></span>|<span data-ttu-id="a5b36-111">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="a5b36-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5b36-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="a5b36-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="a5b36-113">Замените сообщение объекта сообщения на _pMessage,_ которое заменяет сообщение, отозванное предыдущим вызовом [IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md)</span><span class="sxs-lookup"><span data-stu-id="a5b36-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="a5b36-114">Данные в новом сообщении гарантированно будут такие же, как и в отозванных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="a5b36-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="a5b36-115">Сообщение не должно быть помечено как чистое и не должно вызываться после этого вызова [IMAPIViewAdviseSink::OnSaved.](imapiviewadvisesink-onsaved.md)</span><span class="sxs-lookup"><span data-stu-id="a5b36-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="a5b36-116">В случае **успешного вызова SaveCompleted** введите состояние [Normal.](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="a5b36-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="a5b36-117">В противном случае оставайтесь в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="a5b36-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="a5b36-118">Normal или HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="a5b36-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="a5b36-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="a5b36-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="a5b36-120">Установите для последней ошибки E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="a5b36-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="a5b36-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="a5b36-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="a5b36-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="a5b36-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="a5b36-123">Установите для последней ошибки E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="a5b36-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="a5b36-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="a5b36-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="a5b36-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a5b36-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="a5b36-126">Возвращает последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="a5b36-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="a5b36-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="a5b36-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="a5b36-128">Другие [методы IPersistMessage : методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="a5b36-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="a5b36-129">Установите для последней ошибки E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="a5b36-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="a5b36-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="a5b36-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5b36-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a5b36-131">See also</span></span>



[<span data-ttu-id="a5b36-132">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="a5b36-132">Form States</span></span>](form-states.md)

