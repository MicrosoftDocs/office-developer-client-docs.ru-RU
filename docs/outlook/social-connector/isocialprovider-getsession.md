---
title: ИсоЦиалпровидержетсессион
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Получает интерфейс настроенный ISocialSession.
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285774"
---
# <a name="isocialprovidergetsession"></a><span data-ttu-id="54787-103">ISocialProvider::GetSession</span><span class="sxs-lookup"><span data-stu-id="54787-103">ISocialProvider::GetSession</span></span>

<span data-ttu-id="54787-104">Получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="54787-104">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="54787-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="54787-105">Parameters</span></span>

<span data-ttu-id="54787-106">_session_</span><span class="sxs-lookup"><span data-stu-id="54787-106">_session_</span></span>
  
> <span data-ttu-id="54787-107">Интерфейс **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="54787-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54787-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54787-108">Remarks</span></span>

<span data-ttu-id="54787-109">Outlook Social Connector (OSC) использует интерфейс **настроенный ISocialSession** для входа в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="54787-109">The Outlook Social Connector (OSC) uses the **ISocialSession** interface to log on to the social network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54787-110">См. также</span><span class="sxs-lookup"><span data-stu-id="54787-110">See also</span></span>

- [<span data-ttu-id="54787-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54787-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

