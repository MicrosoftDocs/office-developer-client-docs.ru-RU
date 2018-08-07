---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Возвращает строку, представляющую номер версии поставщика для этой социальной сети.
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812734"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="fee1c-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="fee1c-103">ISocialProvider::Version</span></span>

<span data-ttu-id="fee1c-104">Возвращает строку, представляющую номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="fee1c-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="fee1c-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fee1c-105">Property value</span></span>

<span data-ttu-id="fee1c-106">Строка, содержащая номер версии поставщика.</span><span class="sxs-lookup"><span data-stu-id="fee1c-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fee1c-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="fee1c-107">Remarks</span></span>

<span data-ttu-id="fee1c-108">Строка версии следует использовать _MajorVersion_.</span><span class="sxs-lookup"><span data-stu-id="fee1c-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="fee1c-109">Формат _MinorVersion_ (например, 1.4730).</span><span class="sxs-lookup"><span data-stu-id="fee1c-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fee1c-110">См. также</span><span class="sxs-lookup"><span data-stu-id="fee1c-110">See also</span></span>

- [<span data-ttu-id="fee1c-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fee1c-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

