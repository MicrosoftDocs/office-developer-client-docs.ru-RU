---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Возвращает строку, которая содержит коллекцию сведений человека и рисунок для пользователей, указанного с помощью параметра personsAddresses.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812754"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="0bb65-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="0bb65-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="0bb65-104">Возвращает строку, которая содержит коллекцию сведений человека и рисунок для пользователей, указанного с помощью параметра _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="0bb65-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="0bb65-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bb65-105">Parameters</span></span>

<span data-ttu-id="0bb65-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="0bb65-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="0bb65-107">[in] XML-строка, которая указывает хэш SMTP-адреса группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="0bb65-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="0bb65-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="0bb65-108">_personsCollection_</span></span>
  
> <span data-ttu-id="0bb65-109">[out] XML-строка, содержащая набор сведений человека и рисунков.</span><span class="sxs-lookup"><span data-stu-id="0bb65-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0bb65-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="0bb65-110">Remarks</span></span>

<span data-ttu-id="0bb65-111">Outlook Social Connector (OSC) вызывает **GetPeopleDetails** , если поставщик OSC поддерживает синхронизацию по запросу или комбинированным друзья и не.</span><span class="sxs-lookup"><span data-stu-id="0bb65-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="0bb65-112">Параметр _personsAddresses_ должен соответствовать типу определение схемы для **hashedAddresses**, определенных в схеме для расширений поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0bb65-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="0bb65-113">Строка _personsAddresses_ представляет набор хэш SMTP-адреса для каждого пользователя, отображаемые в области пользователей.</span><span class="sxs-lookup"><span data-stu-id="0bb65-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="0bb65-114">Пользователь не нужно быть друга при входе пользователя по свойству [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="0bb65-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="0bb65-115">Хэш SMTP-адреса, шифруются с помощью функции хэширования, указанных в элементе **hashFunction** **возможности** XML.</span><span class="sxs-lookup"><span data-stu-id="0bb65-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="0bb65-116">OSC идентифицирует каждого **hashedAddress** в коллекции _personAddresses_ с элементом **индекса** .</span><span class="sxs-lookup"><span data-stu-id="0bb65-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="0bb65-117">Поставщик должен использовать элемент **индекса** для идентификации получателя **человека** XML при возвращает **друзья** XML для **GetPeopleDetails**.</span><span class="sxs-lookup"><span data-stu-id="0bb65-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="0bb65-118">Если получатель не является зарегистрированным пользователем в социальных сетях, поставщик не должен возвращать любого **пользователя** XML для получателя.</span><span class="sxs-lookup"><span data-stu-id="0bb65-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="0bb65-119">Элемент **индекса** для каждого пользователя сети, представленный **человека** XML соответствует элементу **индекса** для получателя в _personsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="0bb65-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="0bb65-120">OSC хранит данные, возвращенные с помощью параметра _personsCollection_ в памяти.</span><span class="sxs-lookup"><span data-stu-id="0bb65-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="0bb65-121">XML-строка _personsCollection_ код должен соответствовать типу определение схемы для **друзей**, определенных в схеме для расширений поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0bb65-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="0bb65-122">Дополнительные сведения о использует OSC и обновляет эти сведения в памяти можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="0bb65-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0bb65-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0bb65-123">See also</span></span>

- [<span data-ttu-id="0bb65-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bb65-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="0bb65-125">Синхронизация друзей и действия</span><span class="sxs-lookup"><span data-stu-id="0bb65-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

