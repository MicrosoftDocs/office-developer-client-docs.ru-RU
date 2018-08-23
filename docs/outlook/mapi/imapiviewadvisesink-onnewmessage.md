---
title: IMAPIViewAdviseSinkOnNewMessage
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
ms.openlocfilehash: bb373e4b666f44c432ac1b04c0449eb7f0408a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592936"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="f7223-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="f7223-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="f7223-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7223-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7223-105">Уведомляет средство просмотра формы после загрузки, что новое или существующее сообщение в форме.</span><span class="sxs-lookup"><span data-stu-id="f7223-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="f7223-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7223-106">Parameters</span></span>

<span data-ttu-id="f7223-107">None</span><span class="sxs-lookup"><span data-stu-id="f7223-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f7223-108">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f7223-108">Return value</span></span>

<span data-ttu-id="f7223-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f7223-109">S_OK</span></span> 
  
> <span data-ttu-id="f7223-110">Уведомление успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="f7223-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7223-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7223-111">Remarks</span></span>

<span data-ttu-id="f7223-112">Объекты формы вызовите метод **IMAPIViewAdviseSink::OnNewMessage** каждый раз, когда сообщение будет загружен в форму с помощью метода либо [IPersistMessage::InitNew](ipersistmessage-initnew.md) , либо [IPersistMessage::Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="f7223-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f7223-113">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f7223-113">Notes to implementers</span></span>

<span data-ttu-id="f7223-114">Выпуск active указателя на объект формы, так как он больше не указывает на сообщение, которое ранее Просмотр используемого средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="f7223-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="f7223-115">Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f7223-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7223-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f7223-116">See also</span></span>



[<span data-ttu-id="f7223-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7223-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="f7223-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="f7223-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="f7223-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="f7223-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="f7223-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7223-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

