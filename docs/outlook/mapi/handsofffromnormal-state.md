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
# <a name="handsofffromnormal-state"></a><span data-ttu-id="0e115-103">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="0e115-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="0e115-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e115-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e115-105">Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave.](handsoffaftersave-state.md)</span><span class="sxs-lookup"><span data-stu-id="0e115-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="0e115-106">Это часть процесса сохранения содержимого формы в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="0e115-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="0e115-107">Когда в этом состоянии объект формы должен воздерживаться от внесения изменений в копии значений свойств сообщения в памяти, так как не может быть другой возможности сохранить эти изменения.</span><span class="sxs-lookup"><span data-stu-id="0e115-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="0e115-108">В следующей таблице описываются разрешенные переходы из состояния HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="0e115-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="0e115-109">Метод IPersistMessage\*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="0e115-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="0e115-110">**Действие**</span><span class="sxs-lookup"><span data-stu-id="0e115-110">**Action**</span></span>|<span data-ttu-id="0e115-111">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="0e115-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e115-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)_(pMessage!=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="0e115-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="0e115-113">Замените сообщение объекта сообщения  _на pMessage_, которое является заменой сообщения, отозванного предыдущим вызовом [в IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="0e115-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="0e115-114">Данные в новом сообщении гарантированно будут такие же, как и в отозванных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="0e115-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="0e115-115">Сообщение не должно быть помечено как чистое, равно как [и вызов IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="0e115-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="0e115-116">Если вызов **SaveCompleted** удался, введите [нормальное](normal-state.md) состояние.</span><span class="sxs-lookup"><span data-stu-id="0e115-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="0e115-117">В противном случае оставайтесь в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="0e115-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="0e115-118">Нормальный или HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="0e115-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="0e115-119">**IPersistMessage::SaveCompleted**_(pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="0e115-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="0e115-120">Установите последнюю ошибку для E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="0e115-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="0e115-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="0e115-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="0e115-122">**HandsOffMessage,** [IPersistMessage::Save,](ipersistmessage-save.md) [IPersistMessage::InitNew](ipersistmessage-initnew.md)или [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="0e115-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="0e115-123">Установите последнюю ошибку для E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="0e115-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="0e115-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="0e115-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="0e115-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0e115-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="0e115-126">Возвращаем последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="0e115-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="0e115-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="0e115-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="0e115-128">Другие [методы IPersistMessage: методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="0e115-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="0e115-129">Установите последнюю ошибку для E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="0e115-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="0e115-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="0e115-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e115-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0e115-131">See also</span></span>



[<span data-ttu-id="0e115-132">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="0e115-132">Form States</span></span>](form-states.md)

