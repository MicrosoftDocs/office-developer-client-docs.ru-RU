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
# <a name="handsoffaftersave-state"></a><span data-ttu-id="f2c44-103">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="f2c44-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="f2c44-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2c44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2c44-105">Состояние HandsOffAfterSave является частью процесса сохранения содержимого формы в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="f2c44-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="f2c44-106">Когда в этом состоянии объект формы должен воздерживаться от внесения изменений в копии значений свойств сообщения в памяти, так как не может быть другой возможности сохранить эти изменения.</span><span class="sxs-lookup"><span data-stu-id="f2c44-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="f2c44-107">В следующей таблице описываются разрешенные переходы из состояния HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="f2c44-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="f2c44-108">**Метод IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="f2c44-108">**IPersistMessage method**</span></span>|<span data-ttu-id="f2c44-109">**Действие**</span><span class="sxs-lookup"><span data-stu-id="f2c44-109">**Action**</span></span>|<span data-ttu-id="f2c44-110">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="f2c44-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2c44-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)_(pMessage!=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="f2c44-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="f2c44-112">Откройте все встроенные объекты.</span><span class="sxs-lookup"><span data-stu-id="f2c44-112">Open any embedded objects.</span></span> <span data-ttu-id="f2c44-113">Данные в сообщении, хранимом _в pMessage,_ гарантированно будут одинаковыми с данными предыдущего вызова [IPersistMessage:::Save.](ipersistmessage-save.md)</span><span class="sxs-lookup"><span data-stu-id="f2c44-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="f2c44-114">Если вызов **SaveCompleted** удался, введите нормальное состояние.</span><span class="sxs-lookup"><span data-stu-id="f2c44-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="f2c44-115">В противном случае установите последнюю ошибку E_OUTOFMEMORY и оставайтесь в состоянии HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="f2c44-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="f2c44-116">[Нормальный](normal-state.md) или HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="f2c44-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="f2c44-117">**IPersistMessage::SaveCompleted**_(pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="f2c44-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="f2c44-118">Установите последнюю ошибку для E_INVALIDARG или E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="f2c44-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="f2c44-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="f2c44-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="f2c44-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, [или IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="f2c44-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="f2c44-121">Установите последнюю ошибку и верни E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="f2c44-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="f2c44-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="f2c44-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="f2c44-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="f2c44-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="f2c44-124">Загрузить объект формы данными из целевого сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2c44-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="f2c44-125">Этот вызов может произойти, когда объект формы будет отправляться к следующему или предыдущему сообщению в папке.</span><span class="sxs-lookup"><span data-stu-id="f2c44-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="f2c44-126">Normal</span><span class="sxs-lookup"><span data-stu-id="f2c44-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="f2c44-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f2c44-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="f2c44-128">Возвращаем последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="f2c44-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="f2c44-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="f2c44-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="f2c44-130">Другие [методы IPersistMessage: методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="f2c44-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="f2c44-131">Установите последнюю ошибку и верни E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="f2c44-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="f2c44-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="f2c44-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2c44-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f2c44-133">See also</span></span>



[<span data-ttu-id="f2c44-134">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="f2c44-134">Form States</span></span>](form-states.md)

