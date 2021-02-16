---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Получает автоматически настроенный интерфейс ISocialSession.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417443"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="84a7e-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="84a7e-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="84a7e-104">Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="84a7e-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="84a7e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="84a7e-105">Parameters</span></span>

<span data-ttu-id="84a7e-106">_session_</span><span class="sxs-lookup"><span data-stu-id="84a7e-106">_session_</span></span>
  
> <span data-ttu-id="84a7e-107">Интерфейс **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="84a7e-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="84a7e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84a7e-108">Remarks</span></span>

<span data-ttu-id="84a7e-109">Для возвращенного интерфейса **ISocialSession** автоматически выполняется вход в сеть на основании метода поставщика.</span><span class="sxs-lookup"><span data-stu-id="84a7e-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="84a7e-110">Поставщик должен возвратить ошибку OSC_E_NOT_IMPLEMENTED, если социальная сеть не поддерживает автоматическую настройку.</span><span class="sxs-lookup"><span data-stu-id="84a7e-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="84a7e-111">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="84a7e-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84a7e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="84a7e-112">See also</span></span>

- [<span data-ttu-id="84a7e-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84a7e-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

