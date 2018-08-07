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
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809043"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="9b099-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="9b099-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="9b099-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b099-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b099-105">Получает базовый [IMessage: IMAPIProp](imessageimapiprop.md) , это [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) является инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="9b099-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="9b099-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b099-106">Parameters</span></span>

 <span data-ttu-id="9b099-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="9b099-107">_ppmsg_</span></span>
  
> <span data-ttu-id="9b099-108">[out] Объект защищенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9b099-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b099-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="9b099-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9b099-110">S_OK</span></span>
  
> <span data-ttu-id="9b099-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9b099-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b099-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9b099-112">See also</span></span>



[<span data-ttu-id="9b099-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b099-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="9b099-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9b099-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

