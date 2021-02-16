---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Получает строку, представляюную коллекцию людей.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407657"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="3f2f9-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="3f2f9-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="3f2f9-104">Получает строку, представляюную коллекцию людей.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="3f2f9-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f2f9-105">Parameters</span></span>

<span data-ttu-id="3f2f9-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="3f2f9-106">_personsCollection_</span></span>
  
> <span data-ttu-id="3f2f9-107">[out] Строка XML, которая представляет набор друзей человека и соответствует определению друзей в соответствии с XML-схемой для возможности extensibility поставщика Outlook Social Connector (OSC). </span><span class="sxs-lookup"><span data-stu-id="3f2f9-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3f2f9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f2f9-108">Remarks</span></span>

<span data-ttu-id="3f2f9-109">OsC вызывает **GetFriendsAndColleagues,** если поставщик OSC поддерживает кэширование или гибридную синхронизацию друзей в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="3f2f9-110">Когда OSC изначально вызывает метод **GetFriendsAndColleagues** для пользователя Outlook, выехавшего в социальные сети, **GetFriendsAndColleagues** возвращает строку XML, которая представляет друзей во время входа пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="3f2f9-111">Строка XML соответствует определению схемы XML **friends** и определяет элемент person (который также соответствует определению схемы поставщика OSC) для каждого друга. </span><span class="sxs-lookup"><span data-stu-id="3f2f9-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="3f2f9-112">Когда **GetFriendsAndColleagues** возвращает сведения друзей для во время входа пользователя, OSC сохраняет эти сведения в папке контактов.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="3f2f9-113">Эта папка характерна для социальной сети и находится в хранилище Outlook по умолчанию во время входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="3f2f9-114">Дополнительные сведения о том, как OSC кэшировать сведения друзей в папке контактов, см. в подсети "Синхронизация друзей [и действий".](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="3f2f9-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="3f2f9-115">Сведения для каждого друга, возвращаемого в _параметре personsCollection,_ соответствуют определению схемы XML для **человека.**</span><span class="sxs-lookup"><span data-stu-id="3f2f9-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="3f2f9-116">Элемент  person поддерживает множество сведений для каждого друга, в том числе SMTP-адреса электронной почты (которые соподиняются с элементами **emailAddress,** **emailAddress2** и **emailAddress3),** указанные другом в социальной сети, и идентификатор пользователя (который сопоошел с элементом **userID),** который идентифицирует этого друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="3f2f9-117">Чтобы показать действия для пользователя Outlook, выбранного в области "Люди", OSC пытается найти пользователя с каждым другом, возвращенным из **GetFriendsAndColleagues.**</span><span class="sxs-lookup"><span data-stu-id="3f2f9-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="3f2f9-118">OsC делает это, сопобирая SMTP-адрес выбранного пользователя Outlook с адресами электронной почты, указанными каждым другом в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="3f2f9-119">Если OSC находит соответствующий SMTP-адрес электронной почты, osC использует соответствующий **userID** друга для вызова метода [ISocialSession::GetPerson.](isocialsession-getperson.md)</span><span class="sxs-lookup"><span data-stu-id="3f2f9-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="3f2f9-120">Это делается для получения объекта [ISocialPerson](isocialpersoniunknown.md) для этого друга, который затем позволяет OSC получать действия и изображения этого друга из социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="3f2f9-121">Однако если выбранный пользователь Outlook не указывает тот же SMTP-адрес для учетной записи в социальной сети или если у пользователя Outlook нет учетной записи в этой социальной сети, OSC не сможет найти соответствие этому пользователю и не отобразит никаких действий для этого пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f2f9-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f2f9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3f2f9-122">See also</span></span>

- [<span data-ttu-id="3f2f9-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f2f9-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="3f2f9-124">Получение сведений о друзьях</span><span class="sxs-lookup"><span data-stu-id="3f2f9-124">Getting Friends Information</span></span>](getting-friends-information.md)

