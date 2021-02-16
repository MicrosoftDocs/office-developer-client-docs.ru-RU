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
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309718"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="d3beb-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="d3beb-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="d3beb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3beb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3beb-105">Вызывает освобождение текущего сообщения в форме.</span><span class="sxs-lookup"><span data-stu-id="d3beb-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="d3beb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3beb-106">Parameters</span></span>

<span data-ttu-id="d3beb-107">Нет</span><span class="sxs-lookup"><span data-stu-id="d3beb-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d3beb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3beb-108">Return value</span></span>

<span data-ttu-id="d3beb-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3beb-109">S_OK</span></span> 
  
> <span data-ttu-id="d3beb-110">Сообщение успешно освобождено.</span><span class="sxs-lookup"><span data-stu-id="d3beb-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3beb-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3beb-111">Remarks</span></span>

<span data-ttu-id="d3beb-112">Формы переходят в два состояния handsOff:</span><span class="sxs-lookup"><span data-stu-id="d3beb-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="d3beb-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d3beb-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="d3beb-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="d3beb-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="d3beb-115">Когда форма находится в любом из этих состояниях, она находится в процессе постоянного хранения.</span><span class="sxs-lookup"><span data-stu-id="d3beb-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d3beb-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d3beb-116">Notes to implementers</span></span>

<span data-ttu-id="d3beb-117">Когда просматривающая форма вызывает метод **IPersistMessage::HandsOffMessage,** когда форма находится в состоянии [Normal](normal-state.md) или [NoScribble,](noscribble-state.md) рекурсивно вызовите **HandsOffMessage** для каждого сообщения, внедренного в текущее сообщение, и метод [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) для каждого объекта OLE, внедренного в текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="d3beb-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="d3beb-118">Затем отпустите текущее сообщение и все внедренные сообщения и объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="d3beb-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="d3beb-119">Если форма была в обычном состоянии, переходите в состояние HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="d3beb-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="d3beb-120">Если форма была в состоянии NoScribble, переходите в состояние HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="d3beb-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="d3beb-121">После успешного перехода вызовите метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) сообщения и S_OK.</span><span class="sxs-lookup"><span data-stu-id="d3beb-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="d3beb-122">Когда просмотр форм вызывает **HandsOffMessage,** когда форма находится в любом из состояниях handsOff, E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d3beb-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="d3beb-123">Дополнительные сведения о различных состояниях формы см. в [сведениях о состояниях форм.](form-states.md)</span><span class="sxs-lookup"><span data-stu-id="d3beb-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="d3beb-124">Дополнительные сведения о работе с состоянием handsOff объектов хранилища см. в методе [IPersistStorage::HandsOffStorage.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3beb-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3beb-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d3beb-125">See also</span></span>



[<span data-ttu-id="d3beb-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3beb-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="d3beb-127">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="d3beb-127">Form States</span></span>](form-states.md)

