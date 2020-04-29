---
title: исоЦиалсессионунфолловперсон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Удаляет пользователя, определенного параметром userID, в качестве друга в социальной сети.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418437"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="0d319-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="0d319-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="0d319-104">Удаляет пользователя, определенного параметром _UserID_ , в качестве друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d319-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="0d319-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d319-105">Parameters</span></span>

<span data-ttu-id="0d319-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="0d319-106">_userID_</span></span>
  
> <span data-ttu-id="0d319-107">возврата Строка, содержащая идентификатор пользователя социальной сети для человека.</span><span class="sxs-lookup"><span data-stu-id="0d319-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d319-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d319-108">Remarks</span></span>

<span data-ttu-id="0d319-109">Параметр _UserID_ должен быть ДОПУСТИМЫм идентификатором пользователя для пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d319-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="0d319-110">Если у поставщика Outlook Social Connector (OSC) для **возможностей**XML задано **значение** **донотфолловперсон** , поставщик должен возвратить ошибку OSC_E_NOT_FOUND в том случае, если переданный идентификатор пользователя не соответствует пользователю в сети.</span><span class="sxs-lookup"><span data-stu-id="0d319-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="0d319-111">Если поставщик установил для **донотфолловперсон** значение **false** в **возможностях**, поставщик должен возвратить ошибку OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="0d319-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="0d319-112">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0d319-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d319-113">См. также</span><span class="sxs-lookup"><span data-stu-id="0d319-113">See also</span></span>

- [<span data-ttu-id="0d319-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d319-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

