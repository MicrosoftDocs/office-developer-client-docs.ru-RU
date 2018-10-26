---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d246fc0cfc60d0a2b9ff12ee70eae2366cf9b53a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594840"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="3a460-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="3a460-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="3a460-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a460-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a460-105">Получает базовый [IMessage: IMAPIProp](imessageimapiprop.md) , это [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) является инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="3a460-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="3a460-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a460-106">Parameters</span></span>

 <span data-ttu-id="3a460-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="3a460-107">_ppmsg_</span></span>
  
> <span data-ttu-id="3a460-108">[out] Объект защищенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3a460-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3a460-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a460-109">Return value</span></span>

<span data-ttu-id="3a460-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a460-110">S_OK</span></span>
  
> <span data-ttu-id="3a460-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="3a460-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a460-112">См. также</span><span class="sxs-lookup"><span data-stu-id="3a460-112">See also</span></span>



[<span data-ttu-id="3a460-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a460-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="3a460-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3a460-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

