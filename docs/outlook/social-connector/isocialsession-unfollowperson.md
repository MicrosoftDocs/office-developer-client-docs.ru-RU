---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Удаляет лица, указанного с помощью параметра userID как friend в социальных сетях.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812750"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="8c69e-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="8c69e-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="8c69e-104">Удаляет лица, указанного с помощью параметра _userID_ как friend в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="8c69e-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="8c69e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c69e-105">Parameters</span></span>

<span data-ttu-id="8c69e-106">_идентификатор пользователя_</span><span class="sxs-lookup"><span data-stu-id="8c69e-106">_userID_</span></span>
  
> <span data-ttu-id="8c69e-107">[in] Строка, содержащая идентификатор пользователя социальной сети для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c69e-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c69e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c69e-108">Remarks</span></span>

<span data-ttu-id="8c69e-109">Параметр _идентификатор пользователя_ должен быть действительный ID пользователя для пользователя в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="8c69e-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="8c69e-110">Если поставщик Outlook Social Connector (OSC) значение **doNotFollowPerson** как **true** в XML-КОДЕ для **возможностей**, поставщик должен возвращать ошибку OSC_E_NOT_FOUND в случае пользователя, переданный код не соответствует пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="8c69e-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="8c69e-111">Если поставщик значение **doNotFollowPerson** **значение false** в **возможности**, поставщик должен возвращать ошибку OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="8c69e-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="8c69e-112">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8c69e-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c69e-113">См. также</span><span class="sxs-lookup"><span data-stu-id="8c69e-113">See also</span></span>

- [<span data-ttu-id="8c69e-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c69e-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

