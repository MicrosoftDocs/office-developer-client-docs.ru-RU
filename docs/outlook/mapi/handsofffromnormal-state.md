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
ms.openlocfilehash: 92c604c621e2837b76e9e49fd182524ad17fbcac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588344"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="301a5-103">Состояние HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="301a5-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="301a5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="301a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="301a5-105">Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="301a5-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="301a5-106">Он является частью процесс сохранения содержимое формы в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="301a5-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="301a5-107">При работе в это состояние означает, объекта формы следует отказаться от внесения изменений в памяти копии значений свойств сообщений, так как не может быть другой возможности, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="301a5-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="301a5-108">В следующей таблице описываются допустимые переходы из состояния HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="301a5-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="301a5-109">IPersistMessage ** метод **</span><span class="sxs-lookup"><span data-stu-id="301a5-109">****IPersistMessage** method**</span></span>|<span data-ttu-id="301a5-110">**Действие**</span><span class="sxs-lookup"><span data-stu-id="301a5-110">**Action**</span></span>|<span data-ttu-id="301a5-111">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="301a5-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="301a5-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ значение NULL)</span><span class="sxs-lookup"><span data-stu-id="301a5-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="301a5-113">Замените объект message сообщение _pMessage_которого является заменой отозван предыдущего вызова [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)сообщение.</span><span class="sxs-lookup"><span data-stu-id="301a5-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="301a5-114">Данные в новое сообщение гарантированно такой же, как отозванного сообщения.</span><span class="sxs-lookup"><span data-stu-id="301a5-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="301a5-115">Сообщение не должен быть помечен как чистая, а также [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) вызван после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="301a5-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="301a5-116">Если выполнен вызов **SaveCompleted** введите состояние [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="301a5-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="301a5-117">В противном случае остаются в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="301a5-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="301a5-118">Обычный или HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="301a5-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="301a5-119">**IPersistMessage::SaveCompleted** (_pMessage ==_ значение NULL)</span><span class="sxs-lookup"><span data-stu-id="301a5-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="301a5-120">Присвоено значение E_UNEXPECTED последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="301a5-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="301a5-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="301a5-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="301a5-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)или [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="301a5-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="301a5-123">Присвоено значение E_UNEXPECTED последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="301a5-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="301a5-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="301a5-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="301a5-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="301a5-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="301a5-126">Возвращает последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="301a5-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="301a5-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="301a5-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="301a5-128">Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="301a5-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="301a5-129">Присвоено значение E_UNEXPECTED последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="301a5-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="301a5-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="301a5-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="301a5-131">См. также</span><span class="sxs-lookup"><span data-stu-id="301a5-131">See also</span></span>



[<span data-ttu-id="301a5-132">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="301a5-132">Form States</span></span>](form-states.md)

