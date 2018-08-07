---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Получает строку, представляющую идентификатор уникальный социальной сети для подключения к указанной социальных сетей.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812863"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="9f797-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="9f797-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="9f797-104">Получает строку, представляющую идентификатор уникальный социальной сети для подключения к указанной социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="9f797-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="9f797-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f797-105">Parameters</span></span>

<span data-ttu-id="9f797-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="9f797-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="9f797-107">[out] Строка, содержащая идентификатор уникальный социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="9f797-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f797-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="9f797-108">Remarks</span></span>

<span data-ttu-id="9f797-109">Уникальные идентификатор — это строка, идентифицирующая социальных сетей поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="9f797-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="9f797-110">Этот метод может также возвращать значение E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9f797-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f797-111">См. также</span><span class="sxs-lookup"><span data-stu-id="9f797-111">See also</span></span>

- [<span data-ttu-id="9f797-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f797-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

