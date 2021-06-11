---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Добавляет пользователя, идентифицированного параметром emailAddress как друга для зарегистрированного пользователя в социальной сети.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423260"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="694a9-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="694a9-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="694a9-104">Добавляет пользователя, идентифицированного  _параметром emailAddress_ как друга для зарегистрированного пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="694a9-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="694a9-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="694a9-105">Parameters</span></span>

<span data-ttu-id="694a9-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="694a9-106">_emailAddress_</span></span>
  
> <span data-ttu-id="694a9-107">[in] Строка, содержаная адрес электронной почты человека.</span><span class="sxs-lookup"><span data-stu-id="694a9-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="694a9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="694a9-108">Remarks</span></span>

<span data-ttu-id="694a9-109">Параметр  _emailAddress_ должен быть допустимым SMTP-адресом.</span><span class="sxs-lookup"><span data-stu-id="694a9-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="694a9-110">Если поставщик Outlook social Connector (OSC) задает метод  **followPerson** как верный в возможностях, и аргумент для _emailAddress_ не соответствует пользователю в сети, поставщик должен вернуть OSC_E_NOT_FOUND ошибку.</span><span class="sxs-lookup"><span data-stu-id="694a9-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="694a9-111">Если поставщик установил **followPerson** как ложный в возможностях, поставщик должен вернуть OSC_E_FAIL ошибку.  </span><span class="sxs-lookup"><span data-stu-id="694a9-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="694a9-112">Если поставщик реализует [интерфейс ISocialSession2](isocialsession2iunknown.md) и установил **followPerson** как верный в возможностях, OSC будет вызывать [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо  **ISocialSession::FollowPerperson**. </span><span class="sxs-lookup"><span data-stu-id="694a9-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="694a9-113">Если поставщик не реализует интерфейс **ISocialSession2** или **ISocialSession2::FollowPersonEx** возвращает ошибку OSC_E_NOTIMPL, OSC будет вызывать **ISocialSession:::FollowPerson** до тех пор, пока поставщик установил **followPerson** **как** верный в **возможностях**.</span><span class="sxs-lookup"><span data-stu-id="694a9-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="694a9-114">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="694a9-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="694a9-115">При принятии решения о внедрении **ISocalSession:::FollowPerson** или **ISocialSession2::FollowPersonEx** необходимо учитывать, нужны ли вашему поставщику другие методы в **ISocialSession2** и можно ли использовать параметр  _djsplayName_ в **FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="694a9-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="694a9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="694a9-116">See also</span></span>

- [<span data-ttu-id="694a9-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="694a9-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

