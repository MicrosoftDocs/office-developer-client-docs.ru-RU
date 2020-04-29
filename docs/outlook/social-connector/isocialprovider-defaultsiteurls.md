---
title: исоЦиалпровидердефаултситеурлс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Возвращает массив строк, указывающих URL-адреса сайта для поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413775"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="14def-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="14def-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="14def-104">Возвращает массив строк, указывающих URL-адреса сайта для поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="14def-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="14def-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="14def-105">Property value</span></span>

<span data-ttu-id="14def-106">Указатель на структуру, задающую массив строк, которые представляют URL-адреса сайтов для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="14def-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14def-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="14def-107">Remarks</span></span>

<span data-ttu-id="14def-108">Поставщик может поддерживать несколько URL-адресов сайта.</span><span class="sxs-lookup"><span data-stu-id="14def-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="14def-109">OSC задает свойство [настроенный ISocialSession:: SiteUrl](isocialsession-siteurl.md) для информирования поставщика о выбранном URL-адресе сайта.</span><span class="sxs-lookup"><span data-stu-id="14def-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="14def-110">В качестве URL-адреса сайта по умолчанию OSC использует первый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="14def-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="14def-111">Поставщик может возвращать дополнительные элементы в массиве URL-адресов сайта, но OSC не использует их.</span><span class="sxs-lookup"><span data-stu-id="14def-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14def-112">См. также</span><span class="sxs-lookup"><span data-stu-id="14def-112">See also</span></span>

- [<span data-ttu-id="14def-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14def-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

