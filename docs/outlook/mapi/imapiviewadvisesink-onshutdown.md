---
title: имапивиевадвисесинконшутдовн
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
ms.openlocfilehash: b43c1b96130052a05ac390f10f545a66fe72b7fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428524"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="065ae-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="065ae-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="065ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="065ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="065ae-105">Уведомляет средство просмотра форм о том, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="065ae-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="065ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="065ae-106">Parameters</span></span>

<span data-ttu-id="065ae-107">Нет</span><span class="sxs-lookup"><span data-stu-id="065ae-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="065ae-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="065ae-108">Return value</span></span>

<span data-ttu-id="065ae-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="065ae-109">S_OK</span></span> 
  
> <span data-ttu-id="065ae-110">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="065ae-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="065ae-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="065ae-111">Remarks</span></span>

<span data-ttu-id="065ae-112">Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="065ae-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="065ae-113">См. также</span><span class="sxs-lookup"><span data-stu-id="065ae-113">See also</span></span>



[<span data-ttu-id="065ae-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="065ae-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

