---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Добавляет пользователя, определенного параметром emailAddress как friend для пользователя при входе в социальных сетях.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812741"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="360d4-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="360d4-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="360d4-104">Добавляет пользователя, определенного параметром _emailAddress_ как friend для пользователя при входе в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="360d4-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="360d4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="360d4-105">Parameters</span></span>

<span data-ttu-id="360d4-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="360d4-106">_emailAddress_</span></span>
  
> <span data-ttu-id="360d4-107">[in] Строка, содержащая адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="360d4-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="360d4-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="360d4-108">Remarks</span></span>

<span data-ttu-id="360d4-109">Параметр _emailAddress_ должен быть допустимым адресом SMTP.</span><span class="sxs-lookup"><span data-stu-id="360d4-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="360d4-110">Если аргумент для _emailAddress_ не соответствует пользователя в сети поставщика Outlook Social Connector (OSC) Выбор метода **followPerson** **значение true** в **возможности**, поставщик должен возвращать OSC_E_NOT_FOUND Ошибка.</span><span class="sxs-lookup"><span data-stu-id="360d4-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="360d4-111">Если поставщик значение **followPerson** **значение false** в **возможности**, поставщик должен возвращать ошибку OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="360d4-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="360d4-112">Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и установил **followPerson** **значение true** в **возможности**, OSC выполняется звонок [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо **ISocialSession::FollowPerson **.</span><span class="sxs-lookup"><span data-stu-id="360d4-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="360d4-113">Если поставщик не реализует интерфейс **ISocialSession2** или **ISocialSession2::FollowPersonEx** возвращает OSC_E_NOTIMPL ошибка, OSC выполняется звонок **ISocialSession::FollowPerson** до тех пор, пока поставщик установил ** followPerson** как **true** в **возможности**.</span><span class="sxs-lookup"><span data-stu-id="360d4-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="360d4-114">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="360d4-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="360d4-115">В решение о ли для реализации **ISocalSession::FollowPerson** или **ISocialSession2::FollowPersonEx**, следует ли поставщик должен другие методы в **ISocialSession2**и ли вы можете использовать _ djsplayName_ параметр в **FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="360d4-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="360d4-116">См. также</span><span class="sxs-lookup"><span data-stu-id="360d4-116">See also</span></span>

- [<span data-ttu-id="360d4-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="360d4-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

