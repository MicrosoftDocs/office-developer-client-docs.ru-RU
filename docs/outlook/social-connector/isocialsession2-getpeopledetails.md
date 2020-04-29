---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Возвращает строку, содержащую коллекцию сведений о пользователях и изображениях для пользователей, указанных в параметре Персонсаддрессес.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404535"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="01d1a-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="01d1a-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="01d1a-104">Возвращает строку, содержащую коллекцию сведений о пользователях и изображениях для пользователей, указанных в параметре _персонсаддрессес_ .</span><span class="sxs-lookup"><span data-stu-id="01d1a-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="01d1a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="01d1a-105">Parameters</span></span>

<span data-ttu-id="01d1a-106">_персонсаддрессес_</span><span class="sxs-lookup"><span data-stu-id="01d1a-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="01d1a-107">возврата XML-строка, указывающая хэш-адреса SMTP набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="01d1a-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="01d1a-108">_персонсколлектион_</span><span class="sxs-lookup"><span data-stu-id="01d1a-108">_personsCollection_</span></span>
  
> <span data-ttu-id="01d1a-109">вышли XML-строка, содержащая коллекцию сведений о пользователях и изображениях.</span><span class="sxs-lookup"><span data-stu-id="01d1a-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01d1a-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="01d1a-110">Remarks</span></span>

<span data-ttu-id="01d1a-111">Outlook Social Connector (OSC) вызывает **жетпеопледетаилс** , если поставщик OSC поддерживает потребовать или гибридную синхронизацию друзей и не друзей.</span><span class="sxs-lookup"><span data-stu-id="01d1a-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="01d1a-112">Параметр _персонсаддрессес_ должен соответствовать определению схемы для **хашедаддрессес**, как определено в схеме Расширяемость поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="01d1a-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="01d1a-113">Строка _персонсаддрессес_ представляет набор ХЭШИРОВАННЫХ SMTP-адресов для каждого пользователя, отображаемого в области "люди".</span><span class="sxs-lookup"><span data-stu-id="01d1a-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="01d1a-114">Пользователь не должен быть дружественным для вошедшего в систему пользователя, представленного свойством [настроенный ISocialSession:: логжедонусернаме](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="01d1a-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="01d1a-115">Хэшированные SMTP-адреса шифруются с помощью функции хеширования, указанной элементом **хашфунктион** в XML-файле **возможностей** поставщика.</span><span class="sxs-lookup"><span data-stu-id="01d1a-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="01d1a-116">OSC определяет каждый **хашедаддресс** в коллекции _персонаддрессес_ с помощью элемента **index** .</span><span class="sxs-lookup"><span data-stu-id="01d1a-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="01d1a-117">Поставщик должен использовать элемент **index** для определения **пользователя** в XML-коде получателя при возврате XML-кода **друзей** для **жетпеопледетаилс**.</span><span class="sxs-lookup"><span data-stu-id="01d1a-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="01d1a-118">Если получатель не является зарегистрированным пользователем в социальной сети, то поставщик не должен возвращать **XML-** код для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="01d1a-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="01d1a-119">Элемент **index** для каждого пользователя сети, представленного XML-документом **Person** , соответствует элементу **index** для получателя в _персонсаддрессес_.</span><span class="sxs-lookup"><span data-stu-id="01d1a-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="01d1a-120">В файле OSC хранятся сведения, возвращенные параметром _персонсколлектион_ в памяти.</span><span class="sxs-lookup"><span data-stu-id="01d1a-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="01d1a-121">XML-строка _персонсколлектион_ должна соответствовать определению схемы для **друзей**, как определено в схеме Расширяемость поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="01d1a-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="01d1a-122">Для получения дополнительных сведений о том, как OSC использует и обновляет эти сведения в памяти, обратитесь к разделу [Синхронизация друзей и действий](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="01d1a-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01d1a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="01d1a-123">See also</span></span>

- [<span data-ttu-id="01d1a-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01d1a-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="01d1a-125">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="01d1a-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

