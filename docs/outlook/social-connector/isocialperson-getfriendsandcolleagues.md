---
title: исоЦиалперсонжетфриендсандколлеагуес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Получает строку, представляющую коллекцию людей.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407657"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="8b171-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="8b171-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="8b171-104">Получает строку, представляющую коллекцию людей.</span><span class="sxs-lookup"><span data-stu-id="8b171-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="8b171-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b171-105">Parameters</span></span>

<span data-ttu-id="8b171-106">_персонсколлектион_</span><span class="sxs-lookup"><span data-stu-id="8b171-106">_personsCollection_</span></span>
  
> <span data-ttu-id="8b171-107">вышли XML-строка, представляющая набор друзей человека и удовлетворяющая определению **друзей** в соответствии с определением схемы XML для расширяемости поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="8b171-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8b171-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b171-108">Remarks</span></span>

<span data-ttu-id="8b171-109">OSC вызывает **жетфриендсандколлеагуес** , если поставщик OSC поддерживает кэшированную или гибридную синхронизацию друзей в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="8b171-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="8b171-110">Когда OSC вызывает метод **жетфриендсандколлеагуес** для пользователя Outlook, выполнившего вход в социальной сети, **ЖЕТФРИЕНДСАНДКОЛЛЕАГУЕС** возвращает строку XML, которая представляет друзей пользователя, выполнившего вход в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="8b171-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="8b171-111">XML-строка соответствует определению схемы XML **друзей** и указывает элемент **Person** (который также соответствует определению схемы поставщика OSC) для каждого друга.</span><span class="sxs-lookup"><span data-stu-id="8b171-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="8b171-112">Когда **жетфриендсандколлеагуес** возвращает сведения о друзьях для пользователя, вошедшего в систему, OSC сохраняет эти сведения в папке "Контакты".</span><span class="sxs-lookup"><span data-stu-id="8b171-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="8b171-113">Эта папка относится к социальным сетям и находится в магазине Outlook пользователя, вошедшего в систему по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b171-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="8b171-114">Для получения дополнительных сведений о том, как OSC кэширует сведения о друзьях в папке "Контакты", ознакомьтесь со статьей [Синхронизация друзей и действий](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="8b171-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="8b171-115">Сведения для каждого друга, возвращаемого в параметре _персонсколлектион_ , соответствуют определению схемы XML для **пользователя**.</span><span class="sxs-lookup"><span data-stu-id="8b171-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="8b171-116">Элемент **Person** поддерживает множество сведений для каждого друга, в том числе SMTP-адреса электронной почты (которые сопоставляются с элементами **EmailAddress**, **emailAddress2**и **emailAddress3** ), которые друг указал в социальной сети, и идентификатор пользователя (который сопоставляется с элементом **UserID** ), который определяет этого друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="8b171-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="8b171-117">Чтобы отобразить действия для пользователя Outlook, выбранного в области пользователей, OSC пытается найти пользователя с каждым знаком, возвращенным из **жетфриендсандколлеагуес**.</span><span class="sxs-lookup"><span data-stu-id="8b171-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="8b171-118">Это выполняется с помощью файла OSC, который соответствует SMTP-адресу выбранного пользователя Outlook с адресами электронной почты, указанными в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="8b171-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="8b171-119">Если OSC обнаруживает соответствующий SMTP-адрес электронной почты, OSC использует соответствующего **UserID** , чтобы вызвать метод [настроенный ISocialSession::-Person](isocialsession-getperson.md) .</span><span class="sxs-lookup"><span data-stu-id="8b171-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="8b171-120">Это позволяет получить объект [исоЦиалперсон](isocialpersoniunknown.md) для этого друга, который позволяет OSC получать действия и изображения этого друга из социальной сети.</span><span class="sxs-lookup"><span data-stu-id="8b171-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="8b171-121">Тем не менее, если выбранный пользователь Outlook не указывает тот же SMTP-адрес для учетной записи в социальной сети, или если пользователь Outlook не имеет учетной записи в этой социальной сети, OSC не сможет найти соответствующее значение для этого пользователя и не будет отображать действия для этого пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="8b171-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b171-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8b171-122">See also</span></span>

- [<span data-ttu-id="8b171-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b171-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="8b171-124">Получения сведений о друзьях</span><span class="sxs-lookup"><span data-stu-id="8b171-124">Getting Friends Information</span></span>](getting-friends-information.md)

