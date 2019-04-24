---
title: ИсоЦиалсессионжетнетворкидентифиер
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Получает строку, представляющую уникальный идентификатор социальной сети для данного подключения к социальной сети.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285339"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="43c4d-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="43c4d-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="43c4d-104">Получает строку, представляющую уникальный идентификатор социальной сети для данного подключения к социальной сети.</span><span class="sxs-lookup"><span data-stu-id="43c4d-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="43c4d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="43c4d-105">Parameters</span></span>

<span data-ttu-id="43c4d-106">_Нетворкидентифиер_</span><span class="sxs-lookup"><span data-stu-id="43c4d-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="43c4d-107">вышли Строка, содержащая уникальный идентификатор социальной сети.</span><span class="sxs-lookup"><span data-stu-id="43c4d-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43c4d-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="43c4d-108">Remarks</span></span>

<span data-ttu-id="43c4d-109">Уникальный идентификатор сети — это строка, идентифицирующая социальную сеть поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="43c4d-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="43c4d-110">Этот метод также может возвращать E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="43c4d-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43c4d-111">См. также</span><span class="sxs-lookup"><span data-stu-id="43c4d-111">See also</span></span>

- [<span data-ttu-id="43c4d-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43c4d-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

