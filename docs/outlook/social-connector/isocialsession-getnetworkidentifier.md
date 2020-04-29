---
title: исоЦиалсессионжетнетворкидентифиер
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Получает строку, представляющую уникальный идентификатор социальной сети для данного подключения к социальной сети.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433278"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="17ff5-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="17ff5-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="17ff5-104">Получает строку, представляющую уникальный идентификатор социальной сети для данного подключения к социальной сети.</span><span class="sxs-lookup"><span data-stu-id="17ff5-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="17ff5-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="17ff5-105">Parameters</span></span>

<span data-ttu-id="17ff5-106">_нетворкидентифиер_</span><span class="sxs-lookup"><span data-stu-id="17ff5-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="17ff5-107">вышли Строка, содержащая уникальный идентификатор социальной сети.</span><span class="sxs-lookup"><span data-stu-id="17ff5-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17ff5-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="17ff5-108">Remarks</span></span>

<span data-ttu-id="17ff5-109">Уникальный идентификатор сети — это строка, идентифицирующая социальную сеть поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="17ff5-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="17ff5-110">Этот метод также может возвращать E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="17ff5-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17ff5-111">См. также</span><span class="sxs-lookup"><span data-stu-id="17ff5-111">See also</span></span>

- [<span data-ttu-id="17ff5-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17ff5-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

