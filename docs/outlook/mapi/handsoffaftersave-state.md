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
ms.openlocfilehash: 4bc4d680903d81b51a39ed39db3861597443d116
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808577"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="6f737-103">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="6f737-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="6f737-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f737-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f737-105">Состояние HandsOffAfterSave является частью процесс сохранения содержимое формы в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="6f737-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="6f737-106">При работе в это состояние означает, объекта формы следует отказаться от внесения изменений в памяти копии значений свойств сообщений, так как не может быть другой возможности, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="6f737-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="6f737-107">В следующей таблице описываются допустимые переходы из состояния HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="6f737-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="6f737-108">**Метод IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="6f737-108">**IPersistMessage method**</span></span>|<span data-ttu-id="6f737-109">**Действие**</span><span class="sxs-lookup"><span data-stu-id="6f737-109">**Action**</span></span>|<span data-ttu-id="6f737-110">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="6f737-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6f737-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ значение NULL)</span><span class="sxs-lookup"><span data-stu-id="6f737-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="6f737-112">Откройте внедренные объекты.</span><span class="sxs-lookup"><span data-stu-id="6f737-112">Open any embedded objects.</span></span> <span data-ttu-id="6f737-113">Данные в сообщении, хранящиеся в _pMessage_ гарантированно то же, что сообщение в предыдущем вызове [IPersistMessage::Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="6f737-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="6f737-114">Если выполнен вызов **SaveCompleted** введите обычном состоянии.</span><span class="sxs-lookup"><span data-stu-id="6f737-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="6f737-115">В противном случае — значение E_OUTOFMEMORY последней ошибки и всегда оставаться в состоянии HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="6f737-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="6f737-116">[Обычный](normal-state.md) или HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="6f737-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="6f737-117">**IPersistMessage::SaveCompleted** (_pMessage ==_ значение NULL)</span><span class="sxs-lookup"><span data-stu-id="6f737-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="6f737-118">Значение E_INVALIDARG или значение E_UNEXPECTED последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="6f737-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="6f737-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="6f737-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="6f737-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Сохраните**или [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="6f737-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="6f737-121">Значение последней ошибки и возвратить значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="6f737-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="6f737-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="6f737-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="6f737-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="6f737-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="6f737-124">Загрузите объект формы с данными из целевого сообщения.</span><span class="sxs-lookup"><span data-stu-id="6f737-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="6f737-125">Этот вызов может возникнуть при переходе объекта формы в следующий или предыдущий сообщения в папке.</span><span class="sxs-lookup"><span data-stu-id="6f737-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="6f737-126">Normal</span><span class="sxs-lookup"><span data-stu-id="6f737-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="6f737-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6f737-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="6f737-128">Возвращает последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="6f737-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="6f737-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="6f737-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="6f737-130">Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="6f737-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="6f737-131">Значение последней ошибки и возвратить значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="6f737-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="6f737-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="6f737-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f737-133">См. также</span><span class="sxs-lookup"><span data-stu-id="6f737-133">See also</span></span>



[<span data-ttu-id="6f737-134">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="6f737-134">Form States</span></span>](form-states.md)

