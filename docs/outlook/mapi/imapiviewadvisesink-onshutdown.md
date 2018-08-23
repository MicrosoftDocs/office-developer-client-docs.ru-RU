---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f49ea23ed7fef91bcb360483611af2ee60429934
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592971"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="949ae-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="949ae-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="949ae-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="949ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="949ae-105">Уведомляет средство просмотра формы, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="949ae-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="949ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="949ae-106">Parameters</span></span>

<span data-ttu-id="949ae-107">None</span><span class="sxs-lookup"><span data-stu-id="949ae-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="949ae-108">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="949ae-108">Return value</span></span>

<span data-ttu-id="949ae-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="949ae-109">S_OK</span></span> 
  
> <span data-ttu-id="949ae-110">Уведомление успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="949ae-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="949ae-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="949ae-111">Remarks</span></span>

<span data-ttu-id="949ae-112">Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="949ae-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="949ae-113">См. также</span><span class="sxs-lookup"><span data-stu-id="949ae-113">See also</span></span>



[<span data-ttu-id="949ae-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="949ae-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

