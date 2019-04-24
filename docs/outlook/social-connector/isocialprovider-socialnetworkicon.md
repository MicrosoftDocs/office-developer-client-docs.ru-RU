---
title: ИсоЦиалпровидерсоЦиалнетворкикон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Возвращает массив байтов, представляющий значок социальной сети.
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285500"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="b9870-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="b9870-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="b9870-104">Возвращает массив байтов, представляющий значок социальной сети.</span><span class="sxs-lookup"><span data-stu-id="b9870-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="b9870-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b9870-105">Property value</span></span>

<span data-ttu-id="b9870-106">Указатель на структуру, задающую массив байтов, содержащий значок социальной сети.</span><span class="sxs-lookup"><span data-stu-id="b9870-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9870-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9870-107">Remarks</span></span>

<span data-ttu-id="b9870-108">Поддерживаются графические ресурсы форматов BMP, JPEG и PNG.</span><span class="sxs-lookup"><span data-stu-id="b9870-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9870-109">См. также</span><span class="sxs-lookup"><span data-stu-id="b9870-109">See also</span></span>

- [<span data-ttu-id="b9870-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9870-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

