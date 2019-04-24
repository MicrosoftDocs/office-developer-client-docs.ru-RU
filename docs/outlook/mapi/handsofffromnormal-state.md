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
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299470"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="7392a-103">Состояние HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7392a-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="7392a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7392a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7392a-105">Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="7392a-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="7392a-106">Это часть процесса сохранения содержимого формы в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="7392a-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="7392a-107">В этом состоянии объект Form должен относиться к изменениям копий значений свойств сообщения в памяти, так как эти изменения могут быть недоступны другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="7392a-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="7392a-108">В следующей таблице описаны допустимые переходы из состояния HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="7392a-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="7392a-109">Иперсистмессаже \* \* метод \* \*</span><span class="sxs-lookup"><span data-stu-id="7392a-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="7392a-110">**Действие**</span><span class="sxs-lookup"><span data-stu-id="7392a-110">**Action**</span></span>|<span data-ttu-id="7392a-111">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="7392a-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7392a-112">[Иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md) (_пмессаже! =_ null)</span><span class="sxs-lookup"><span data-stu-id="7392a-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="7392a-113">Замените сообщение объекта Message на _пмессаже_, заменяющее сообщение, которое было отозвано предыдущим вызовом метода [Иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="7392a-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="7392a-114">Данные в новом сообщении гарантированно совпадают с теми, что и в отозванном сообщении.</span><span class="sxs-lookup"><span data-stu-id="7392a-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="7392a-115">Сообщение не должно быть помечено как Clean, и не должно [имапивиевадвисесинк:: OnSave](imapiviewadvisesink-onsaved.md) вызывается после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="7392a-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="7392a-116">Если вызов **савекомплетед** выполнен успешно, введите нормальное [](normal-state.md) состояние.</span><span class="sxs-lookup"><span data-stu-id="7392a-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="7392a-117">В противном случае Оставайтесь в состоянии HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="7392a-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="7392a-118">Обычный или HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7392a-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="7392a-119">**Иперсистмессаже:: савекомплетед** (_пмессаже = =_ null)</span><span class="sxs-lookup"><span data-stu-id="7392a-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="7392a-120">Задайте для последней ошибки значение Е_УНЕКСПЕКТЕД.</span><span class="sxs-lookup"><span data-stu-id="7392a-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7392a-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7392a-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="7392a-122">**Хандсоффмессаже**, [Иперсистмессаже:: Save](ipersistmessage-save.md), [Иперсистмессаже:: Инитнев](ipersistmessage-initnew.md)или [иперсистмессаже:: Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="7392a-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="7392a-123">Задайте для последней ошибки значение Е_УНЕКСПЕКТЕД.</span><span class="sxs-lookup"><span data-stu-id="7392a-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7392a-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7392a-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="7392a-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7392a-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="7392a-126">Возврат последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="7392a-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="7392a-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7392a-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="7392a-128">Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="7392a-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="7392a-129">Задайте для последней ошибки значение Е_УНЕКСПЕКТЕД.</span><span class="sxs-lookup"><span data-stu-id="7392a-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7392a-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7392a-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7392a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7392a-131">See also</span></span>



[<span data-ttu-id="7392a-132">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="7392a-132">Form States</span></span>](form-states.md)

