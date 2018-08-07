---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера для пользователя в ходе проверки подлинности web.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812736"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="94c63-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="94c63-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="94c63-104">Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера для пользователя в ходе проверки подлинности web.</span><span class="sxs-lookup"><span data-stu-id="94c63-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="94c63-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="94c63-105">Parameters</span></span>

<span data-ttu-id="94c63-106">_URL-адрес_</span><span class="sxs-lookup"><span data-stu-id="94c63-106">_url_</span></span>
  
> <span data-ttu-id="94c63-107">[out] Строка, содержащая URL-адрес для формы, используемые в веб-проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="94c63-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94c63-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="94c63-108">Remarks</span></span>

<span data-ttu-id="94c63-109">После форма будет предоставлен пользователю, метод [ISocialSession::LogonWeb](isocialsession-logonweb.md) вызывается с пустая строка для параметра _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="94c63-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94c63-110">См. также</span><span class="sxs-lookup"><span data-stu-id="94c63-110">See also</span></span>

- [<span data-ttu-id="94c63-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94c63-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

