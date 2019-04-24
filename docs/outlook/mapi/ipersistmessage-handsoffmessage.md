---
title: Иперсистмессажехандсоффмессаже
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
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="74eb1-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="74eb1-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="74eb1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74eb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74eb1-105">Заставляет форму выпустить текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="74eb1-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="74eb1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74eb1-106">Parameters</span></span>

<span data-ttu-id="74eb1-107">Нет</span><span class="sxs-lookup"><span data-stu-id="74eb1-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="74eb1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74eb1-108">Return value</span></span>

<span data-ttu-id="74eb1-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="74eb1-109">S_OK</span></span> 
  
> <span data-ttu-id="74eb1-110">Сообщение успешно выпущено.</span><span class="sxs-lookup"><span data-stu-id="74eb1-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74eb1-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="74eb1-111">Remarks</span></span>

<span data-ttu-id="74eb1-112">Формы переходят на два состояния Хандсофф:</span><span class="sxs-lookup"><span data-stu-id="74eb1-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="74eb1-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="74eb1-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="74eb1-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="74eb1-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="74eb1-115">Если форма находится в любом из этих состояний, она находится в процессе окончательного сохранения.</span><span class="sxs-lookup"><span data-stu-id="74eb1-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="74eb1-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="74eb1-116">Notes to implementers</span></span>

<span data-ttu-id="74eb1-117">Когда средство просмотра формы вызывает метод **иперсистмессаже:: хандсоффмессаже** , когда форма находится в обычном [](normal-state.md) или нерисованном состоянии, рекурсивно вызовите **хандсоффмессаже** для каждого сообщения, внедренного в текущее сообщение, и [](noscribble-state.md) [ Иперсистстораже:: метод Хандсоффстораже](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) для каждого объекта OLE, внедренного в текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="74eb1-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="74eb1-118">Затем отпустите текущее сообщение и все внедренные сообщения и объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="74eb1-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="74eb1-119">Если форма находилась в нормальном состоянии, переходите в состояние HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="74eb1-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="74eb1-120">Если форма находилась в состоянии Scribble, переходите в состояние HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="74eb1-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="74eb1-121">После успешного перехода вызовите метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) сообщения и ВОЗВРАТИТ значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="74eb1-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="74eb1-122">Когда средство просмотра формы вызывает **хандсоффмессаже** , когда форма находится в любом из состояний хандсофф, возвращайте е_унекспектед.</span><span class="sxs-lookup"><span data-stu-id="74eb1-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="74eb1-123">Дополнительные сведения о различных состояниях формы можно узнать в статье [состояния форм](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="74eb1-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="74eb1-124">Дополнительные сведения о том, как работать с состоянием объектов хранилища Хандсофф, можно узнать в методе [иперсистстораже:: хандсоффстораже](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) .</span><span class="sxs-lookup"><span data-stu-id="74eb1-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74eb1-125">См. также</span><span class="sxs-lookup"><span data-stu-id="74eb1-125">See also</span></span>



[<span data-ttu-id="74eb1-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74eb1-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="74eb1-127">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="74eb1-127">Form States</span></span>](form-states.md)

