---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Удаляет пользователя, которого задан параметр userID как друга в социальной сети.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418437"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="ef48c-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="ef48c-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="ef48c-104">Удаляет пользователя, которого задан параметр  _userID_ как друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef48c-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="ef48c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef48c-105">Parameters</span></span>

<span data-ttu-id="ef48c-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="ef48c-106">_userID_</span></span>
  
> <span data-ttu-id="ef48c-107">[in] Строка, содержаная ИД пользователя социальной сети для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef48c-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef48c-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef48c-108">Remarks</span></span>

<span data-ttu-id="ef48c-109">Параметр  _userID_ должен быть действительным ИД пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef48c-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="ef48c-110">Если поставщик Outlook Social Connector (OSC) установил для **doNotFollowPerson** в XML-интерфейсе для возможностей **true,** поставщик должен возвращать ошибку OSC_E_NOT_FOUND, если переданный ид пользователя не соответствует пользователю в сети. </span><span class="sxs-lookup"><span data-stu-id="ef48c-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="ef48c-111">Если поставщик установил для **doNotFollowPerson** в качестве false в возможностях, поставщик должен вернуть OSC_E_FAIL ошибку.  </span><span class="sxs-lookup"><span data-stu-id="ef48c-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="ef48c-112">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ef48c-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef48c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ef48c-113">See also</span></span>

- [<span data-ttu-id="ef48c-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef48c-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

