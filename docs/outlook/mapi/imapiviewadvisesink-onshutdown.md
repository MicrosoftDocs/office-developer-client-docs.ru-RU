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
ms.openlocfilehash: 2a09731dbd0ba2c5d6c1055a7c5ed11097c5ef27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809239"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="4b2b3-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="4b2b3-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="4b2b3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b2b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b2b3-105">Уведомляет средство просмотра формы, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="4b2b3-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="4b2b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b2b3-106">Parameters</span></span>

<span data-ttu-id="4b2b3-107">Нет</span><span class="sxs-lookup"><span data-stu-id="4b2b3-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="4b2b3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="4b2b3-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4b2b3-109">S_OK</span></span> 
  
> <span data-ttu-id="4b2b3-110">Уведомление успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="4b2b3-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b2b3-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b2b3-111">Remarks</span></span>

<span data-ttu-id="4b2b3-112">Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="4b2b3-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b2b3-113">См. также</span><span class="sxs-lookup"><span data-stu-id="4b2b3-113">See also</span></span>



[<span data-ttu-id="4b2b3-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b2b3-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

