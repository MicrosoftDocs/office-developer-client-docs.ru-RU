---
title: ИсоЦиалпровидерверсион
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Возвращает строку, представляющую номер версии поставщика для этой социальной сети.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285387"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="b36b6-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="b36b6-103">ISocialProvider::Version</span></span>

<span data-ttu-id="b36b6-104">Возвращает строку, представляющую номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="b36b6-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="b36b6-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b36b6-105">Property value</span></span>

<span data-ttu-id="b36b6-106">Строка, содержащая номер версии поставщика.</span><span class="sxs-lookup"><span data-stu-id="b36b6-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b36b6-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="b36b6-107">Remarks</span></span>

<span data-ttu-id="b36b6-108">В строке версии должен использоваться параметр _majorversion_.</span><span class="sxs-lookup"><span data-stu-id="b36b6-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="b36b6-109">Формат _minorversion_ (например, 1,4730).</span><span class="sxs-lookup"><span data-stu-id="b36b6-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b36b6-110">См. также</span><span class="sxs-lookup"><span data-stu-id="b36b6-110">See also</span></span>

- [<span data-ttu-id="b36b6-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b36b6-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

