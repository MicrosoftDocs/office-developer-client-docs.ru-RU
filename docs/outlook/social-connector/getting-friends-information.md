---
title: Получение сведений о друзьях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'Outlook Social Connector (OSC) вызывает метод ИсоЦиалпровидер:: capabilities, который определяет возможности поставщика OSC для социальной сети.'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286324"
---
# <a name="getting-friends-information"></a><span data-ttu-id="f16f7-103">Получение сведений о друзьях</span><span class="sxs-lookup"><span data-stu-id="f16f7-103">Getting friends information</span></span>

<span data-ttu-id="f16f7-104">Outlook Social Connector (OSC) вызывает метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который определяет возможности поставщика OSC для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="f16f7-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="f16f7-105">Если элементы \*\*\*\* **качефриендс и** в возвращенном XML- \*\*\*\* коде имеют значение, указывающее, что поставщик OSC поддерживает получать и кэшировать друзей как элементы контактов Outlook в соответствующей папке "Контакты", OSC может выполнить Следующая последовательность вызовов.</span><span class="sxs-lookup"><span data-stu-id="f16f7-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="f16f7-106">OSC вызывает методы в этой последовательности для получения сведений и изображений (как поддерживается интерфейсом [исоЦиалперсон](isocialpersoniunknown.md) ) для друзей в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="f16f7-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f16f7-107">OSC обновляет кэш с интервалом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f16f7-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="f16f7-108">Если во время обновления кэша возникает ошибка, перемещается на другой заданный интервал, который также можно контролировать, указав элемент **контактсинкрестартинтервал** в XML-коде **возможностей** .</span><span class="sxs-lookup"><span data-stu-id="f16f7-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="f16f7-109">Дополнительные сведения об обновлении кэша контактов приведены в статье [Синхронизация друзей и действий](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="f16f7-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="f16f7-110">[Настроенный ISocialSession:: логжедонусерид](isocialsession-loggedonuserid.md) — получает идентификатор пользователя Office, который вошел в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="f16f7-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="f16f7-111">[Настроенный ISocialSession::-Person](isocialsession-getperson.md) — с помощью идентификатора пользователя Office, OSC получает объект **исоЦиалперсон** для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f16f7-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="f16f7-112">[ИсоЦиалперсон:: жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md) — этот OSC получает список дружественных пользователей в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="f16f7-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="f16f7-113">[Настроенный ISocialSession::-Person](isocialsession-getperson.md) — для каждого пользователя в XML-файле, возвращенного **жетфриендсандколлеагуес**, OSC получает интерфейс **исоЦиалперсон** .</span><span class="sxs-lookup"><span data-stu-id="f16f7-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="f16f7-114">[ИсоЦиалперсон::](isocialperson-getpicture.md) жетфриендсандколлеагуес — для каждого пользователя в XML-файле, возвращаемого методом \*\*\*\*, OSC получает ресурс изображения.</span><span class="sxs-lookup"><span data-stu-id="f16f7-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f16f7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f16f7-115">See also</span></span>

- [<span data-ttu-id="f16f7-116">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="f16f7-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="f16f7-117">ПереOSC типичные последовательности вызовов</span><span class="sxs-lookup"><span data-stu-id="f16f7-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

