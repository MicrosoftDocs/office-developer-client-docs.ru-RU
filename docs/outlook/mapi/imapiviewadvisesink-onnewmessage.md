---
title: Имапивиевадвисесинконневмессаже
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328793"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="848fb-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="848fb-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="848fb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="848fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="848fb-105">Уведомляет средство просмотра форм о том, что в форме загружено новое или существующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="848fb-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="848fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="848fb-106">Parameters</span></span>

<span data-ttu-id="848fb-107">Нет</span><span class="sxs-lookup"><span data-stu-id="848fb-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="848fb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="848fb-108">Return value</span></span>

<span data-ttu-id="848fb-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="848fb-109">S_OK</span></span> 
  
> <span data-ttu-id="848fb-110">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="848fb-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="848fb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="848fb-111">Remarks</span></span>

<span data-ttu-id="848fb-112">Объекты формы вызывают метод **имапивиевадвисесинк:: онневмессаже** при каждом загрузке сообщения в форме с помощью метода [Иперсистмессаже:: инитнев](ipersistmessage-initnew.md) или [иперсистмессаже:: Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="848fb-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="848fb-113">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="848fb-113">Notes to implementers</span></span>

<span data-ttu-id="848fb-114">Освободите активный указатель на объект формы, так как он больше не указывает на сообщение, которое ранее было проходило в вашем средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="848fb-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="848fb-115">Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="848fb-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="848fb-116">См. также</span><span class="sxs-lookup"><span data-stu-id="848fb-116">See also</span></span>



[<span data-ttu-id="848fb-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="848fb-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="848fb-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="848fb-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="848fb-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="848fb-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="848fb-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="848fb-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

