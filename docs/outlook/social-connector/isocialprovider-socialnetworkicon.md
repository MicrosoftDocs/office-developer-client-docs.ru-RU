---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Возвращает массив байтов, который представляет значок для социальных сетей.
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812859"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="7bd0e-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="7bd0e-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="7bd0e-104">Возвращает массив байтов, который представляет значок для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="7bd0e-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="7bd0e-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7bd0e-105">Property value</span></span>

<span data-ttu-id="7bd0e-106">Указатель на структуру, которая указывает массив байтов, который содержит значок для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="7bd0e-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7bd0e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="7bd0e-107">Remarks</span></span>

<span data-ttu-id="7bd0e-108">Поддерживаемые изображение ресурсов, BMP, .jpeg и .png форматы.</span><span class="sxs-lookup"><span data-stu-id="7bd0e-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7bd0e-109">См. также</span><span class="sxs-lookup"><span data-stu-id="7bd0e-109">See also</span></span>

- [<span data-ttu-id="7bd0e-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7bd0e-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

