---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Возвращает строку, которая содержит коллекцию сведений о пользователе и изображении для пользователей, указанных параметром personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404535"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="03246-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="03246-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="03246-104">Возвращает строку, которая содержит коллекцию сведений о пользователе и изображении для пользователей, указанных _параметром personsAddresses._</span><span class="sxs-lookup"><span data-stu-id="03246-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="03246-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="03246-105">Parameters</span></span>

<span data-ttu-id="03246-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="03246-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="03246-107">[in] Строка XML, которая указывает smTP-адреса с hashed для набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="03246-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="03246-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="03246-108">_personsCollection_</span></span>
  
> <span data-ttu-id="03246-109">[out] Строка XML, которая содержит коллекцию сведений о человеке и изображении.</span><span class="sxs-lookup"><span data-stu-id="03246-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03246-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="03246-110">Remarks</span></span>

<span data-ttu-id="03246-111">Outlook Social Connector (OSC) вызывает **GetPeopleDetails,** если поставщик OSC поддерживает синхронизацию друзей и других пользователей по требованию или гибридную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="03246-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="03246-112">Параметр  _personsAddresses должен_ соответствовать определению схемы для **hashedAddresses,** как определено в схеме для возможности extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="03246-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="03246-113">Строка  _personsAddresses_ представляет собой набор адресов SMTP с hashed для каждого пользователя, отображаемого в области "Люди".</span><span class="sxs-lookup"><span data-stu-id="03246-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="03246-114">Пользователь не должен быть другом во время входа пользователя, представленного свойством [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md)</span><span class="sxs-lookup"><span data-stu-id="03246-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="03246-115">Hashed SMTP-адреса шифруются с помощью функции hashing, указанной элементом **hashFunction** в **XML** возможностей поставщика.</span><span class="sxs-lookup"><span data-stu-id="03246-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="03246-116">OsC идентифицирует каждый **hashedAddress** в коллекции _personAddresses_ с помощью **элемента индекса.**</span><span class="sxs-lookup"><span data-stu-id="03246-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="03246-117">Поставщик должен использовать элемент **индекса** для  идентификации XML-данных получателя при возвращении XML-данных друзей **для GetPeopleDetails.** </span><span class="sxs-lookup"><span data-stu-id="03246-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="03246-118">Если получатель не зарегистрирован в социальной сети, поставщик не должен возвращать **никаких** XML-данных для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="03246-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="03246-119">Элемент **индекса** для каждого сетевого пользователя, представленного пользователем **XML,** соответствует элементу **индекса** получателя в _personsAddresses._</span><span class="sxs-lookup"><span data-stu-id="03246-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="03246-120">OsC сохраняет сведения, возвращенные  _параметром personsCollection,_ в памяти.</span><span class="sxs-lookup"><span data-stu-id="03246-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="03246-121">_XML-строка personsCollection_ должна соответствовать определению схемы для друзей, как определено в схеме для возможности extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="03246-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="03246-122">Дополнительные сведения о том, как OSC использует и обновляет эти сведения в памяти, см. в подсети "Синхронизация друзей [и действий".](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="03246-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03246-123">См. также</span><span class="sxs-lookup"><span data-stu-id="03246-123">See also</span></span>

- [<span data-ttu-id="03246-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03246-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="03246-125">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="03246-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

