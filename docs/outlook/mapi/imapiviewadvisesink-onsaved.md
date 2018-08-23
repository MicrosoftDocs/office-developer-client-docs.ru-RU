---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ae94b40d984adee0f3c888f69dfdbffb1e352e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584438"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="cf1a1-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="cf1a1-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="cf1a1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf1a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf1a1-105">Уведомляет средство просмотра формы, который был сохранен текущего сообщения в форме.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="cf1a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf1a1-106">Parameters</span></span>

<span data-ttu-id="cf1a1-107">None</span><span class="sxs-lookup"><span data-stu-id="cf1a1-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="cf1a1-108">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cf1a1-108">Return value</span></span>

<span data-ttu-id="cf1a1-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="cf1a1-109">S_OK</span></span> 
  
> <span data-ttu-id="cf1a1-110">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf1a1-111">���������</span><span class="sxs-lookup"><span data-stu-id="cf1a1-111">Remarks</span></span>

<span data-ttu-id="cf1a1-112">Объект формы вызывает метод **IMAPIViewAdviseSink::OnSaved** после сохранения текущего сообщения в форме.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="cf1a1-113">Это позволяет использовать средства просмотра для обновления их windows сведения об изменениях в сообщение.</span><span class="sxs-lookup"><span data-stu-id="cf1a1-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="cf1a1-114">Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="cf1a1-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf1a1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="cf1a1-115">See also</span></span>



[<span data-ttu-id="cf1a1-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf1a1-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

