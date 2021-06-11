---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Получает строку, описываемую возможностями поставщика.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408105"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="7b649-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="7b649-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="7b649-104">Получает строку, описываемую возможностями поставщика.</span><span class="sxs-lookup"><span data-stu-id="7b649-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="7b649-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="7b649-105">Parameters</span></span>

<span data-ttu-id="7b649-106">_result_</span><span class="sxs-lookup"><span data-stu-id="7b649-106">_result_</span></span>
  
> <span data-ttu-id="7b649-107">[вышел] Строка XML, которая представляет возможности поставщика Outlook social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="7b649-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b649-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b649-108">Remarks</span></span>

<span data-ttu-id="7b649-109">Строка _XML_ возвращаемого результата должна соответствовать  определению схемы элемента возможностей, как определено в схеме XML для extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="7b649-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="7b649-110">Поставщик должен вернуть строку  _результатов,_ чтобы обеспечить правильную работу последующих вызовов из OSC к поставщику.</span><span class="sxs-lookup"><span data-stu-id="7b649-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b649-111">См. также</span><span class="sxs-lookup"><span data-stu-id="7b649-111">See also</span></span>

- [<span data-ttu-id="7b649-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b649-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

