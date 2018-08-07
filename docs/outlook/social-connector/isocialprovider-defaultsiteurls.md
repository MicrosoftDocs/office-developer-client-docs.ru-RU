---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Возвращает массив строк, которые задают URL-адресов сайта для поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812719"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="a5596-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="a5596-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="a5596-104">Возвращает массив строк, которые задают URL-адресов сайта для поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="a5596-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="a5596-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a5596-105">Property value</span></span>

<span data-ttu-id="a5596-106">Указатель на структуру, которая указывает массив строк, представляющих URL-адресов сайта для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="a5596-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5596-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5596-107">Remarks</span></span>

<span data-ttu-id="a5596-108">Поставщик может поддерживать несколько URL-адресов сайта.</span><span class="sxs-lookup"><span data-stu-id="a5596-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="a5596-109">OSC задает свойство [ISocialSession::SiteUrl](isocialsession-siteurl.md) для оповещения поставщика URL-адрес выбранного сайта.</span><span class="sxs-lookup"><span data-stu-id="a5596-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="a5596-110">Первый элемент массива используется OSC как URL-адрес сайта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5596-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="a5596-111">Поставщик может возвращать дополнительные элементы в массиве URL-адрес сайта, но OSC не использует их.</span><span class="sxs-lookup"><span data-stu-id="a5596-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5596-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a5596-112">See also</span></span>

- [<span data-ttu-id="a5596-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5596-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

