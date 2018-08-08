---
title: Получение сведений о друзьях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook Social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальных сетей.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812706"
---
# <a name="getting-friends-information"></a><span data-ttu-id="91e1d-103">Получение сведений о друзьях</span><span class="sxs-lookup"><span data-stu-id="91e1d-103">Getting friends information</span></span>

<span data-ttu-id="91e1d-104">Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , чтобы определить возможности поставщика OSC для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="91e1d-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="91e1d-105">Если элементы **getFriends** и **cacheFriends** в возвращенные **возможности** XML показывают, что поставщика OSC поддерживает получение друзей и элементы в соответствующей папке контактов контактов кэширования друзья как Outlook, можно сделать OSC следующую последовательность вызова.</span><span class="sxs-lookup"><span data-stu-id="91e1d-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="91e1d-106">OSC вызывает методы в следующем порядке, чтобы получить сведения и рисунки (как поддерживаемый интерфейс [ISocialPerson](isocialpersoniunknown.md) ) для друзей в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="91e1d-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="91e1d-107">OSC обновляет кэш с интервалом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91e1d-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="91e1d-108">При возникновении ошибки во время кэша обновите, повторных попыток OSC в другой предварительно интервала, что также можно управлять путем указания элемент **contactSyncRestartInterval** в **возможности** XML.</span><span class="sxs-lookup"><span data-stu-id="91e1d-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="91e1d-109">Дополнительные сведения об обновлении кэша контакты можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="91e1d-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="91e1d-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — OSC Получает идентификатор пользователя Office, который вошел в систему социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="91e1d-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="91e1d-111">[ISocialSession::GetPerson](isocialsession-getperson.md) , используя идентификатор пользователя Microsoft Office, OSC возвращает объект **ISocialPerson** для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="91e1d-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="91e1d-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — OSC Получает список friend пользователя в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="91e1d-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="91e1d-113">[ISocialSession::GetPerson](isocialsession-getperson.md) — для каждого пользователя в XML-код возвращает **GetFriendsAndColleagues**, OSC получает интерфейс **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="91e1d-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="91e1d-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) — для каждого пользователя в XML-код возвращает **GetFriendsAndColleagues**, OSC получает ресурсов изображений.</span><span class="sxs-lookup"><span data-stu-id="91e1d-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91e1d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="91e1d-115">See also</span></span>

- [<span data-ttu-id="91e1d-116">XML-код для возможности</span><span class="sxs-lookup"><span data-stu-id="91e1d-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="91e1d-117">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="91e1d-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

