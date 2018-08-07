---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fd7e3b1d1284cdf4451330aabcce8fd0279ad5ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809485"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="a706d-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="a706d-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="a706d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a706d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a706d-105">Приводит к освобождение сообщения, его текущей формы.</span><span class="sxs-lookup"><span data-stu-id="a706d-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="a706d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a706d-106">Parameters</span></span>

<span data-ttu-id="a706d-107">Нет</span><span class="sxs-lookup"><span data-stu-id="a706d-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a706d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="a706d-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a706d-109">S_OK</span></span> 
  
> <span data-ttu-id="a706d-110">Сообщение было успешно отправлено.</span><span class="sxs-lookup"><span data-stu-id="a706d-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a706d-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="a706d-111">Remarks</span></span>

<span data-ttu-id="a706d-112">Перенос форм в двух HandsOff состояниях:</span><span class="sxs-lookup"><span data-stu-id="a706d-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="a706d-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="a706d-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="a706d-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="a706d-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="a706d-115">При открытии формы в одном из следующих состояний, находится в процессе хранением без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="a706d-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a706d-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a706d-116">Notes to implementers</span></span>

<span data-ttu-id="a706d-117">Когда форма просмотра вызывает метод **IPersistMessage::HandsOffMessage** , пока форма находится в состоянии [Normal](normal-state.md) или [NoScribble](noscribble-state.md) , рекурсивно вызова **HandsOffMessage** для каждого сообщения, внедренной в текущего сообщения и [ IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) метод для каждого объекта OLE, внедренные в текущем сообщении.</span><span class="sxs-lookup"><span data-stu-id="a706d-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="a706d-118">Затем release текущего сообщения и всех внедренных сообщений и объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="a706d-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="a706d-119">Если форма была в обычном состоянии переход в состояние HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="a706d-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="a706d-120">Если форма была в состоянии NoScribble переход в состояние HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="a706d-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="a706d-121">После успешного перехода вызовите метод [функции IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) сообщение и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="a706d-121">After a successful transition, call the message's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="a706d-122">Когда форма просмотра вызывает **HandsOffMessage** при формы в одном из состояний HandsOff, возвратите значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="a706d-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="a706d-123">Дополнительные сведения о состояниях формы можно [Состояния формы](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="a706d-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="a706d-124">Дополнительные сведения о работе с состоянием HandsOff объектов хранилища [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) см.</span><span class="sxs-lookup"><span data-stu-id="a706d-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a706d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a706d-125">See also</span></span>



[<span data-ttu-id="a706d-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a706d-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="a706d-127">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="a706d-127">Form States</span></span>](form-states.md)

