---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Получает строку, представляющую сведений для пользователя, такие как имя, Фамилия и URL-адрес изображения профилей.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812716"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="a282f-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="a282f-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="a282f-104">Получает строку, представляющую сведений для пользователя, такие как имя, Фамилия и URL-адрес изображения профилей.</span><span class="sxs-lookup"><span data-stu-id="a282f-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="a282f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a282f-105">Parameters</span></span>

<span data-ttu-id="a282f-106">_Подробные сведения_</span><span class="sxs-lookup"><span data-stu-id="a282f-106">_details_</span></span>
  
> <span data-ttu-id="a282f-107">[out] Строковое значение XML, представляющий сведения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="a282f-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a282f-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="a282f-108">Remarks</span></span>

<span data-ttu-id="a282f-109">XML-строка, возвращаемых _сведений_ , должен соответствовать требованиям определение схемы для **человека**, определенных в схеме для расширений поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="a282f-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="a282f-110">Вызовов OSC **GetDetails** Если кэширования для поддержки поставщика OSC или синхронизации гибридного друзей в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="a282f-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="a282f-111">При OSC изначально получает друзей действия для пользователя, выполнившего вход, он вызывает [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)и сохранение информации друзей в папке контактов, характерные для социальных сетей в хранилище Outlook по умолчанию пользователя, выполнившего вход .</span><span class="sxs-lookup"><span data-stu-id="a282f-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="a282f-112">Впоследствии OSC не вызывает **GetFriendsAndColleagues** или **GetDetails** Если не истек интервал обновления кэша.</span><span class="sxs-lookup"><span data-stu-id="a282f-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="a282f-113">Дополнительные сведения о как OSC кэширует сведения друзей в папке контактов можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="a282f-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a282f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a282f-114">See also</span></span>

- [<span data-ttu-id="a282f-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a282f-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

