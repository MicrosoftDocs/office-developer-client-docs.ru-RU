---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Добавляет пользователя, идентифицируемого параметрами emailAddresses и displayName, как Friend для вошедшего в сеть пользователя в социальной сети.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429833"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="519a6-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="519a6-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="519a6-104">Добавляет пользователя, идентифицируемого параметрами _EmailAddresses_ и _DisplayName_ , как Friend для вошедшего в сеть пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="519a6-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="519a6-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="519a6-105">Parameters</span></span>

<span data-ttu-id="519a6-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="519a6-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="519a6-107">возврата Массив, содержащий один или несколько допустимых SMTP-адресов для пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="519a6-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="519a6-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="519a6-108">_displayName_</span></span>
  
> <span data-ttu-id="519a6-109">возврата Строка, содержащая отображаемое имя человека, которого требуется добавить в качестве друга.</span><span class="sxs-lookup"><span data-stu-id="519a6-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="519a6-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="519a6-110">Remarks</span></span>

<span data-ttu-id="519a6-111">Если Outlook Social Connector (OSC) предоставляет более чем адрес SMTP в массиве параметра **EmailAddresses** , то поставщик OSC может предположить, что первый элемент является основным SMTP-адресом.</span><span class="sxs-lookup"><span data-stu-id="519a6-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="519a6-112">Если у поставщика для элемента **фолловперсон** в XML-файле **возможностей** задано **значение true** , а ни один из элементов для _EmailAddresses_ не соответствует пользователю в сети, то поставщик должен возвратить ошибку OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="519a6-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="519a6-113">Если поставщик установил для **фолловперсон** значение **false** в **возможностях**, поставщик должен возвратить ошибку OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="519a6-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="519a6-114">Если метод **фолловперсонекс** завершается успешно, поставщик может использовать строку в параметре _DisplayName_ , чтобы обращаться к пользователю во всех последующих сообщениях с дружественным подтверждением, а не по адресу SMTP.</span><span class="sxs-lookup"><span data-stu-id="519a6-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="519a6-115">С другой стороны, поставщик должен уметь обрабатывать OSC, передающий пустую строку для параметра _DisplayName_ .</span><span class="sxs-lookup"><span data-stu-id="519a6-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="519a6-116">Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и присвоить **фолловперсон** значение **true** в XML-коде возможностей, то OSC вызывает **фолловперсонекс** вместо [настроенный ISocialSession:: фолловперсон](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="519a6-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="519a6-117">Если у поставщика задано **followPerson** значение фолловперсон **, но не** реализуется интерфейс **ISocialSession2** , или **фолловперсонекс** возвращает ошибку OSC_E_NOTIMPL, OSC вызывает метод **настроенный ISocialSession:: фолловперсон**.</span><span class="sxs-lookup"><span data-stu-id="519a6-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="519a6-118">См. также</span><span class="sxs-lookup"><span data-stu-id="519a6-118">See also</span></span>

- [<span data-ttu-id="519a6-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="519a6-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

