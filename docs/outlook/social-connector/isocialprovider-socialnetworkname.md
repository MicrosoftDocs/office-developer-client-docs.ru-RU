---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Возвращает строку, представляющую имя социальной сети.
ms.openlocfilehash: 78424db0940b2c23914355b2b20ba5bc531ad3ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812733"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="1cd7e-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="1cd7e-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="1cd7e-104">Возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="1cd7e-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="1cd7e-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1cd7e-105">Property value</span></span>

<span data-ttu-id="1cd7e-106">Строка, содержащая имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="1cd7e-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1cd7e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="1cd7e-107">Remarks</span></span>

<span data-ttu-id="1cd7e-108">Outlook Social Connector (OSC) поставщиков должны локализация имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="1cd7e-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1cd7e-109">См. также</span><span class="sxs-lookup"><span data-stu-id="1cd7e-109">See also</span></span>

- [<span data-ttu-id="1cd7e-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cd7e-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

