---
title: исоЦиалпровидержетсессион
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Получает интерфейс настроенный ISocialSession.
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419550"
---
# <a name="isocialprovidergetsession"></a><span data-ttu-id="a6e3a-103">ISocialProvider::GetSession</span><span class="sxs-lookup"><span data-stu-id="a6e3a-103">ISocialProvider::GetSession</span></span>

<span data-ttu-id="a6e3a-104">Получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a6e3a-104">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="a6e3a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6e3a-105">Parameters</span></span>

<span data-ttu-id="a6e3a-106">_session_</span><span class="sxs-lookup"><span data-stu-id="a6e3a-106">_session_</span></span>
  
> <span data-ttu-id="a6e3a-107">Интерфейс **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="a6e3a-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a6e3a-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6e3a-108">Remarks</span></span>

<span data-ttu-id="a6e3a-109">Outlook Social Connector (OSC) использует интерфейс **настроенный ISocialSession** для входа в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a6e3a-109">The Outlook Social Connector (OSC) uses the **ISocialSession** interface to log on to the social network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6e3a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a6e3a-110">See also</span></span>

- [<span data-ttu-id="a6e3a-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6e3a-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

