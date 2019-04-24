---
title: Имаписекуремессажежетбасемессаже
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
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322395"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="56f8b-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="56f8b-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="56f8b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56f8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56f8b-105">Получает базовый [iMessage: IMAPIProp](imessageimapiprop.md) , который инкапсулируется этим [Имаписекуремессаже: интерфейс IUnknown](imapisecuremessageiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="56f8b-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="56f8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56f8b-106">Parameters</span></span>

 <span data-ttu-id="56f8b-107">_ппмсг_</span><span class="sxs-lookup"><span data-stu-id="56f8b-107">_ppmsg_</span></span>
  
> <span data-ttu-id="56f8b-108">вышли Объект защищенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="56f8b-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56f8b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56f8b-109">Return value</span></span>

<span data-ttu-id="56f8b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="56f8b-110">S_OK</span></span>
  
> <span data-ttu-id="56f8b-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="56f8b-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56f8b-112">См. также</span><span class="sxs-lookup"><span data-stu-id="56f8b-112">See also</span></span>



[<span data-ttu-id="56f8b-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="56f8b-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="56f8b-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="56f8b-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

