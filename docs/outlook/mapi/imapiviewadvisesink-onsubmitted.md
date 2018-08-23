---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579447"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="d67a7-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="d67a7-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="d67a7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d67a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d67a7-105">Уведомляет средство просмотра формы, что текущего сообщения были отправлены диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="d67a7-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="d67a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d67a7-106">Parameters</span></span>

<span data-ttu-id="d67a7-107">None</span><span class="sxs-lookup"><span data-stu-id="d67a7-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d67a7-108">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d67a7-108">Return value</span></span>

<span data-ttu-id="d67a7-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d67a7-109">S_OK</span></span> 
  
> <span data-ttu-id="d67a7-110">Уведомление успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="d67a7-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d67a7-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="d67a7-111">Remarks</span></span>

<span data-ttu-id="d67a7-112">Объект формы вызывает метод **IMAPIViewAdviseSink::OnSubmitted** после успешного возврата вызова [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="d67a7-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d67a7-113">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d67a7-113">Notes to implementers</span></span>

<span data-ttu-id="d67a7-114">После вызова **OnSubmitted** можно продолжить предполагается, что сообщение были обновлены.</span><span class="sxs-lookup"><span data-stu-id="d67a7-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="d67a7-115">Обновление windows в соответствии с все изменения, произошедшие.</span><span class="sxs-lookup"><span data-stu-id="d67a7-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="d67a7-116">Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d67a7-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d67a7-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d67a7-117">See also</span></span>



[<span data-ttu-id="d67a7-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d67a7-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="d67a7-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d67a7-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

