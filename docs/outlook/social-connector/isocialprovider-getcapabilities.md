---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Получает строку, которая описывает возможности поставщика.
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812729"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="16ad8-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="16ad8-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="16ad8-104">Получает строку, которая описывает возможности поставщика.</span><span class="sxs-lookup"><span data-stu-id="16ad8-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="16ad8-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="16ad8-105">Parameters</span></span>

<span data-ttu-id="16ad8-106">_результат_</span><span class="sxs-lookup"><span data-stu-id="16ad8-106">_result_</span></span>
  
> <span data-ttu-id="16ad8-107">[out] XML-строка, которая представляет возможности поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="16ad8-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16ad8-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="16ad8-108">Remarks</span></span>

<span data-ttu-id="16ad8-109">XML-строка возвращаемый _результат_ должен соответствовать требованиям определение схемы для элемента **capabilities** , как определено в XML-схему для расширений поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="16ad8-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="16ad8-110">Поставщик должен возвращать строку _результатов_ для включения последующие вызовы от OSC к поставщику для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="16ad8-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16ad8-111">См. также</span><span class="sxs-lookup"><span data-stu-id="16ad8-111">See also</span></span>

- [<span data-ttu-id="16ad8-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16ad8-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

