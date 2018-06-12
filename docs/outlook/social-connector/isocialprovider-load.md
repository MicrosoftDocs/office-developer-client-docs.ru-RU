---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Инициализирует поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812731"
---
# <a name="isocialproviderload"></a><span data-ttu-id="dba81-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="dba81-103">ISocialProvider::Load</span></span>

<span data-ttu-id="dba81-104">Инициализирует поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="dba81-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="dba81-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="dba81-105">Parameters</span></span>

<span data-ttu-id="dba81-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="dba81-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="dba81-107">[in] Версия интерфейсы поставщика OSC, ожидаемый OSC.</span><span class="sxs-lookup"><span data-stu-id="dba81-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="dba81-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="dba81-108">_languageTag_</span></span>
  
> <span data-ttu-id="dba81-109">[in] Тег языка IETF Internet Engineering Task Force (), определенные в [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) и [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), представляющий текущий язык пользовательского интерфейса Outlook.</span><span class="sxs-lookup"><span data-stu-id="dba81-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dba81-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="dba81-110">Remarks</span></span>

<span data-ttu-id="dba81-111">Версия формата для параметра _socialProviderInterfaceVersion_ составляет _X_. _xxxx_, где _X_ — это основной версии и _xxxx_ — это дополнительный номер версии OSC.</span><span class="sxs-lookup"><span data-stu-id="dba81-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="dba81-112">Office 2013 Проверьте основной номер версии, 15.</span><span class="sxs-lookup"><span data-stu-id="dba81-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dba81-113">См. также</span><span class="sxs-lookup"><span data-stu-id="dba81-113">See also</span></span>

- [<span data-ttu-id="dba81-114">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dba81-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

