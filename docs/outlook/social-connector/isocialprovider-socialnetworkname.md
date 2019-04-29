---
title: ИсоЦиалпровидерсоЦиалнетворкнаме
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Возвращает строку, представляющую имя социальной сети.
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406880"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="90777-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="90777-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="90777-104">Возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="90777-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="90777-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="90777-105">Property value</span></span>

<span data-ttu-id="90777-106">Строка, содержащая имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="90777-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90777-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="90777-107">Remarks</span></span>

<span data-ttu-id="90777-108">Поставщики Outlook Social Connector (OSC) должны локализовать имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="90777-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90777-109">См. также</span><span class="sxs-lookup"><span data-stu-id="90777-109">See also</span></span>

- [<span data-ttu-id="90777-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90777-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

