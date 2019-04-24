---
title: Имапивиевадвисесинконшутдовн
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351165"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="05198-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="05198-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="05198-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05198-105">Уведомляет средство просмотра форм о том, что форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="05198-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="05198-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05198-106">Parameters</span></span>

<span data-ttu-id="05198-107">Нет</span><span class="sxs-lookup"><span data-stu-id="05198-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="05198-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05198-108">Return value</span></span>

<span data-ttu-id="05198-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="05198-109">S_OK</span></span> 
  
> <span data-ttu-id="05198-110">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="05198-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05198-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="05198-111">Remarks</span></span>

<span data-ttu-id="05198-112">Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="05198-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05198-113">См. также</span><span class="sxs-lookup"><span data-stu-id="05198-113">See also</span></span>



[<span data-ttu-id="05198-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05198-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

