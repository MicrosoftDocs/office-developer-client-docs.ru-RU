---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Возвращает массив строк, которые указывают URL-адреса сайта для Outlook поставщика социальных соединителов (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413775"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="0d4cd-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="0d4cd-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="0d4cd-104">Возвращает массив строк, которые указывают URL-адреса сайта для Outlook поставщика социальных соединителов (OSC).</span><span class="sxs-lookup"><span data-stu-id="0d4cd-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="0d4cd-105">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0d4cd-105">Property value</span></span>

<span data-ttu-id="0d4cd-106">Указатель на структуру, которая указывает массив строк, которые представляют URL-адреса сайтов для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0d4cd-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d4cd-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d4cd-107">Remarks</span></span>

<span data-ttu-id="0d4cd-108">Поставщик может поддерживать несколько URL-адресов сайтов.</span><span class="sxs-lookup"><span data-stu-id="0d4cd-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="0d4cd-109">OsC задает [свойство ISocialSession::SiteUrl](isocialsession-siteurl.md) для информирования поставщика выбранного URL-адреса сайта.</span><span class="sxs-lookup"><span data-stu-id="0d4cd-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="0d4cd-110">OsC использует первый элемент массива в качестве URL-адреса сайта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d4cd-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="0d4cd-111">Поставщик может возвращать дополнительные элементы в массив URL-адресов сайта, но OSC не использует их.</span><span class="sxs-lookup"><span data-stu-id="0d4cd-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d4cd-112">См. также</span><span class="sxs-lookup"><span data-stu-id="0d4cd-112">See also</span></span>

- [<span data-ttu-id="0d4cd-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d4cd-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

