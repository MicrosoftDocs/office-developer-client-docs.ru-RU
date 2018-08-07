---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Добавляет лица, указанного с помощью параметров emailAddresses и displayName как friend для пользователя при входе в социальных сетях.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812759"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="1194e-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="1194e-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="1194e-104">Добавляет лица, указанного с помощью параметров _emailAddresses_ и _displayName_ как friend для пользователя при входе в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="1194e-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="1194e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="1194e-105">Parameters</span></span>

<span data-ttu-id="1194e-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="1194e-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="1194e-107">[in] Массив, содержащий один или несколько допустимый SMTP-адреса для пользователя в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="1194e-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="1194e-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="1194e-108">_displayName_</span></span>
  
> <span data-ttu-id="1194e-109">[in] Строка, содержащая отображаемое имя пользователя, добавляемого в качестве friend.</span><span class="sxs-lookup"><span data-stu-id="1194e-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1194e-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="1194e-110">Remarks</span></span>

<span data-ttu-id="1194e-111">Если Outlook Social Connector (OSC) обеспечивает более чем на SMTP-адрес в массиве с помощью параметра **emailAddresses** поставщика OSC можно предположить, что первый элемент является основной SMTP-адрес.</span><span class="sxs-lookup"><span data-stu-id="1194e-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="1194e-112">Если поставщик установил элемент **followPerson** **значение true** в **возможности** XML, а ни один из элементов для _emailAddresses_ не соответствует пользователя в сети, поставщик должен возвращать ошибку OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="1194e-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="1194e-113">Если поставщик значение **followPerson** **значение false** в **возможности**, поставщик должен возвращать ошибку OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="1194e-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="1194e-114">При успешном применении метода **FollowPersonEx** поставщик может использовать строки с помощью параметра _displayName_ устранения человека в любой последующих friend подтверждения электронной почты, а не с адресом SMTP-адресов пользователя.</span><span class="sxs-lookup"><span data-stu-id="1194e-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="1194e-115">С другой стороны поставщик должен быть обрабатывать OSC, передаче пустой строки для параметра _displayName_ .</span><span class="sxs-lookup"><span data-stu-id="1194e-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="1194e-116">Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и установил **followPerson** как **true** в возможности XML, OSC вызывает **FollowPersonEx** вместо [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="1194e-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="1194e-117">Если поставщик **followPerson** задано **значение true** , но не реализует интерфейс **ISocialSession2** или **FollowPersonEx** возвращает OSC_E_NOTIMPL ошибка, OSC вызывает **ISocialSession::FollowPerson**.</span><span class="sxs-lookup"><span data-stu-id="1194e-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1194e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="1194e-118">See also</span></span>

- [<span data-ttu-id="1194e-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1194e-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

