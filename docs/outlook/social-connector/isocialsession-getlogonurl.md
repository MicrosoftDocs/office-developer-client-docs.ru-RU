---
title: ИсоЦиалсессионжетлогонурл
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера пользователю во время веб-проверки подлинности.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285380"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="17f11-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="17f11-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="17f11-104">Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера пользователю во время веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="17f11-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="17f11-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="17f11-105">Parameters</span></span>

<span data-ttu-id="17f11-106">_url_</span><span class="sxs-lookup"><span data-stu-id="17f11-106">_url_</span></span>
  
> <span data-ttu-id="17f11-107">вышли Строка, содержащая URL-адрес для формы, используемой при веб-проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="17f11-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17f11-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="17f11-108">Remarks</span></span>

<span data-ttu-id="17f11-109">После того как форма представлена пользователю, метод [настроенный ISocialSession:: логонвеб](isocialsession-logonweb.md) вызывается с пустой строкой для параметра _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="17f11-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17f11-110">См. также</span><span class="sxs-lookup"><span data-stu-id="17f11-110">See also</span></span>

- [<span data-ttu-id="17f11-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17f11-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

