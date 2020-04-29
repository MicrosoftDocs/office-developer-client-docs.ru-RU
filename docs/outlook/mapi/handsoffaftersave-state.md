---
title: Состояние HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406607"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="7f2fb-103">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="7f2fb-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="7f2fb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f2fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f2fb-105">Состояние HandsOffAfterSave является частью процесса сохранения содержимого формы в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="7f2fb-106">В этом состоянии объект Form должен относиться к изменениям копий значений свойств сообщения в памяти, так как эти изменения могут быть недоступны другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="7f2fb-107">В следующей таблице описаны допустимые переходы из состояния HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="7f2fb-108">**Метод Иперсистмессаже**</span><span class="sxs-lookup"><span data-stu-id="7f2fb-108">**IPersistMessage method**</span></span>|<span data-ttu-id="7f2fb-109">**Действие**</span><span class="sxs-lookup"><span data-stu-id="7f2fb-109">**Action**</span></span>|<span data-ttu-id="7f2fb-110">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="7f2fb-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f2fb-111">[Иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md)(_пмессаже! =_ null)</span><span class="sxs-lookup"><span data-stu-id="7f2fb-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="7f2fb-112">Откройте все внедренные объекты.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-112">Open any embedded objects.</span></span> <span data-ttu-id="7f2fb-113">Данные в сообщениях, хранящихся в _пмессаже_ , гарантированно совпадают с сообщением в предыдущем вызове [Иперсистмессаже:: Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="7f2fb-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="7f2fb-114">Если вызов **савекомплетед** выполнен успешно, введите нормальное состояние.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="7f2fb-115">В противном случае присвойте последней ошибке E_OUTOFMEMORY и оставайтесь в состоянии HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="7f2fb-116">[Обычный](normal-state.md) или HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="7f2fb-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="7f2fb-117">**Иперсистмессаже:: савекомплетед**(_пмессаже = =_ null)</span><span class="sxs-lookup"><span data-stu-id="7f2fb-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="7f2fb-118">Задайте для последней ошибки значение E_INVALIDARG или E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7f2fb-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="7f2fb-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="7f2fb-120">[Иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md), **Save**или [иперсистмессаже:: инитнев](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="7f2fb-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="7f2fb-121">Установка последней ошибки и возврат E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7f2fb-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="7f2fb-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="7f2fb-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="7f2fb-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="7f2fb-124">Загрузка объекта Form с данными из целевого сообщения.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="7f2fb-125">Этот вызов может произойти, когда объект Form переходит к следующему или предыдущему сообщению в папке.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="7f2fb-126">Normal</span><span class="sxs-lookup"><span data-stu-id="7f2fb-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="7f2fb-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7f2fb-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="7f2fb-128">Возврат последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="7f2fb-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="7f2fb-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="7f2fb-130">Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="7f2fb-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="7f2fb-131">Установка последней ошибки и возврат E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7f2fb-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7f2fb-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="7f2fb-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f2fb-133">См. также</span><span class="sxs-lookup"><span data-stu-id="7f2fb-133">See also</span></span>



[<span data-ttu-id="7f2fb-134">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="7f2fb-134">Form States</span></span>](form-states.md)

