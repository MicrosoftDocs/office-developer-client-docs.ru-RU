---
title: ИсоЦиалпровидерсоЦиалнетворкгуид
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407874"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="4e420-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="4e420-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="4e420-104">Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="4e420-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="4e420-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4e420-105">Property value</span></span>

<span data-ttu-id="4e420-106">Указатель на значение GUID, которое представляет уникальный идентификатор для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="4e420-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e420-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e420-107">Remarks</span></span>

<span data-ttu-id="4e420-108">GUID должен быть неизменяемым и не должен изменяться, даже если версия поставщика изменяется.</span><span class="sxs-lookup"><span data-stu-id="4e420-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e420-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4e420-109">See also</span></span>

- [<span data-ttu-id="4e420-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e420-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

