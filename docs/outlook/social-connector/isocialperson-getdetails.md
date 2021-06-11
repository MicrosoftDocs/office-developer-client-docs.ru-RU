---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Получает строку, которая представляет сведения для пользователя, например имя, фамилию и URL-адрес к изображению профиля.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427334"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="8994e-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="8994e-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="8994e-104">Получает строку, которая представляет сведения для пользователя, например имя, фамилию и URL-адрес к изображению профиля.</span><span class="sxs-lookup"><span data-stu-id="8994e-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="8994e-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="8994e-105">Parameters</span></span>

<span data-ttu-id="8994e-106">_details_</span><span class="sxs-lookup"><span data-stu-id="8994e-106">_details_</span></span>
  
> <span data-ttu-id="8994e-107">[вышел] Значение строки XML, которое представляет сведения для человека.</span><span class="sxs-lookup"><span data-stu-id="8994e-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8994e-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="8994e-108">Remarks</span></span>

<span data-ttu-id="8994e-109">Возвращаемая  строка XML-данных должна соответствовать определению схемы для **человека,** как определено в схеме для Outlook поставщика социальных соединителем (OSC).</span><span class="sxs-lookup"><span data-stu-id="8994e-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="8994e-110">OsC вызывает **GetDetails,** если поставщик OSC поддерживает кэширование или гибридную синхронизацию друзей в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="8994e-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="8994e-111">Когда OSC сначала получает действия друзей для зарегистрированного пользователя, он вызывает [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)и хранит сведения друзей в папке контактов, определенной социальной сети, в журнале в хранилище по умолчанию Outlook пользователя.</span><span class="sxs-lookup"><span data-stu-id="8994e-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="8994e-112">Впоследствии OSC не вызывает **GetFriendsAndColleagues** или **GetDetails,** если истек срок действия интервала обновления кэша.</span><span class="sxs-lookup"><span data-stu-id="8994e-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="8994e-113">Дополнительные сведения о том, как osC кэшировать сведения друзей в папке контактов, см. в руб. [Синхронизация друзей и действий.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="8994e-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8994e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8994e-114">See also</span></span>

- [<span data-ttu-id="8994e-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8994e-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

