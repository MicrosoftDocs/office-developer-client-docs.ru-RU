---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Добавляет пользователя, идентифицированного по параметрам emailAddresses и displayName, в качестве друга во время входа пользователя в социальной сети.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429833"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="911a1-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="911a1-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="911a1-104">Добавляет пользователя, идентифицированного по  _параметрам emailAddresses_ и  _displayName,_ в качестве друга во время входа пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="911a1-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="911a1-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="911a1-105">Parameters</span></span>

<span data-ttu-id="911a1-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="911a1-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="911a1-107">[in] Массив, содержащий один или несколько допустимых SMTP-адресов для человека в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="911a1-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="911a1-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="911a1-108">_displayName_</span></span>
  
> <span data-ttu-id="911a1-109">[in] Строка с отображаемой именем человека, добавляемого в качестве друга.</span><span class="sxs-lookup"><span data-stu-id="911a1-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="911a1-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="911a1-110">Remarks</span></span>

<span data-ttu-id="911a1-111">Если Outlook Social Connector (OSC) предоставляет больше, чем smTP-адрес в массиве в параметре **emailAddresses,** поставщик OSC может предположить, что первый элемент является основным SMTP-адресом.</span><span class="sxs-lookup"><span data-stu-id="911a1-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="911a1-112">Если поставщик установил для элемента **followPerson** в **XML** возможностей true и ни один из элементов _emailAddresses_ не соответствует пользователю в сети, поставщик должен вернуть OSC_E_NOT_FOUND ошибку. </span><span class="sxs-lookup"><span data-stu-id="911a1-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="911a1-113">Если поставщик установил **для followPerson в** возможностях false, поставщик должен вернуть OSC_E_FAIL ошибку.  </span><span class="sxs-lookup"><span data-stu-id="911a1-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="911a1-114">Если метод **FollowPersonEx** успешно используется, поставщик может использовать строку в параметре  _displayName_ для обращения к человеку в любом последующем сообщении электронной почты подтверждения друга, а не адресовать его по SMTP-адресу.</span><span class="sxs-lookup"><span data-stu-id="911a1-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="911a1-115">С другой стороны, поставщик должен иметь возможность обрабатывать OSC, передав пустую строку для _параметра displayName._</span><span class="sxs-lookup"><span data-stu-id="911a1-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="911a1-116">Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и установил для  **followPerson** в XML возможностей true, OSC вызывает **FollowPersonEx** вместо [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="911a1-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="911a1-117">Если поставщик установил для **followPerson** true, но не реализует интерфейс **ISocialSession2** или **FollowPersonEx** возвращает ошибку OSC_E_NOTIMPL, OSC вызывает **ISocialSession::FollowPerson**. </span><span class="sxs-lookup"><span data-stu-id="911a1-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="911a1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="911a1-118">See also</span></span>

- [<span data-ttu-id="911a1-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="911a1-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

