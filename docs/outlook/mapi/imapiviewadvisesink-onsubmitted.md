---
title: Имапивиевадвисесинконсубмиттед
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
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433985"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="6e4de-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="6e4de-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="6e4de-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e4de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e4de-105">Уведомляет средство просмотра форм о том, что текущее сообщение было отправлено в Диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e4de-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="6e4de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e4de-106">Parameters</span></span>

<span data-ttu-id="6e4de-107">Нет</span><span class="sxs-lookup"><span data-stu-id="6e4de-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6e4de-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e4de-108">Return value</span></span>

<span data-ttu-id="6e4de-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e4de-109">S_OK</span></span> 
  
> <span data-ttu-id="6e4de-110">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="6e4de-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e4de-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="6e4de-111">Remarks</span></span>

<span data-ttu-id="6e4de-112">Объект Form вызывает метод **имапивиевадвисесинк::** onsubmittedся после вызова [Имапимессажесите:: субмитмессаже](imapimessagesite-submitmessage.md) успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="6e4de-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6e4de-113">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="6e4de-113">Notes to implementers</span></span>

<span data-ttu-id="6e4de-114">После \*\*\*\* вызова OnSubmitted можно продолжить предположение о том, что сообщение было обновлено.</span><span class="sxs-lookup"><span data-stu-id="6e4de-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="6e4de-115">Обновите Windows, чтобы отразить все произошедшие изменения.</span><span class="sxs-lookup"><span data-stu-id="6e4de-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="6e4de-116">Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6e4de-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e4de-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6e4de-117">See also</span></span>



[<span data-ttu-id="6e4de-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="6e4de-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="6e4de-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e4de-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

