---
title: Пример XML друзей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: Пример XML в этом разделе — строка XML друга, возвращаемая в Outlook Social Connector (OSC) после вызова метода ISocialPerson::GetFriendsAndColleagues. В примере показано, как друзья XML для двух друзей, каждый из которых делимитирован элементом person. Каждый друг указывает уникальное значение элемента userID в социальной сети.
ms.openlocfilehash: 593019ec4dcd1b9b578bfe275fb8e6664bbd11a9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542228"
---
# <a name="friends-xml-example"></a><span data-ttu-id="00295-105">Пример XML друзей</span><span class="sxs-lookup"><span data-stu-id="00295-105">Friends XML example</span></span>

<span data-ttu-id="00295-106">Пример XML в этом разделе — строка XML друга, возвращенная в Outlook Social Connector (OSC) после вызова метода [ISocialPerson::GetFriendsAndColleagues.](isocialperson-getfriendsandcolleagues.md)</span><span class="sxs-lookup"><span data-stu-id="00295-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="00295-107">В примере **показано, как друзья** XML для двух друзей, каждый из которых делимитирован **элементом person.**</span><span class="sxs-lookup"><span data-stu-id="00295-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="00295-108">Каждый друг указывает уникальное значение элемента **userID** в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="00295-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="00295-109">Остальные элементы XML **друзей** имеют понятные имена.</span><span class="sxs-lookup"><span data-stu-id="00295-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="00295-110">Подробные сведения об этих элементах см. в [XML для друзей.](xml-for-friends.md)</span><span class="sxs-lookup"><span data-stu-id="00295-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="00295-111">Пример XML</span><span class="sxs-lookup"><span data-stu-id="00295-111">XML example</span></span>

<span data-ttu-id="00295-112">В следующем примере показаны **XML** друзей для двух пользователей в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="00295-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a><span data-ttu-id="00295-113">См. также</span><span class="sxs-lookup"><span data-stu-id="00295-113">See also</span></span>

- [<span data-ttu-id="00295-114">Примеры XML поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="00295-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="00295-115">Пример XML возможностей</span><span class="sxs-lookup"><span data-stu-id="00295-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="00295-116">Пример ленты действий XML</span><span class="sxs-lookup"><span data-stu-id="00295-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="00295-117">Outlook Схема поставщика социальных соединителем XML</span><span class="sxs-lookup"><span data-stu-id="00295-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

