---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Получает строку, представляющую коллекцию людей.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812725"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="3635c-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="3635c-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="3635c-104">Получает строку, представляющую коллекцию людей.</span><span class="sxs-lookup"><span data-stu-id="3635c-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="3635c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="3635c-105">Parameters</span></span>

<span data-ttu-id="3635c-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="3635c-106">_personsCollection_</span></span>
  
> <span data-ttu-id="3635c-107">[out] XML-строка, которая представляет набор друзья человека, и, который соответствует определения **друзья** , определенных в схеме XML для расширений поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="3635c-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3635c-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3635c-108">Remarks</span></span>

<span data-ttu-id="3635c-109">Вызовов OSC **GetFriendsAndColleagues** Если кэширования для поддержки поставщика OSC или синхронизации гибридного друзей в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="3635c-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="3635c-110">Когда OSC изначально вызывает метод **GetFriendsAndColleagues** для Outlook пользователя, выполнившего вход в социальной сети, **GetFriendsAndColleagues** возвращает XML-строка, которая представляет друзей пользователя, вошедшего в систему в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="3635c-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="3635c-111">XML-строка соответствует определение схемы XML **друзей** и задает элемент **человека** (который также соответствует определение схемы поставщика OSC) для каждого друга.</span><span class="sxs-lookup"><span data-stu-id="3635c-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="3635c-112">При отображении **GetFriendsAndColleagues** друзья сведений для пользователя, вошедшего в систему, OSC сохраняет их в папке «Контакты».</span><span class="sxs-lookup"><span data-stu-id="3635c-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="3635c-113">Эта папка специально для социальных сетей и при входе пользователя в хранилище Outlook по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3635c-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="3635c-114">Дополнительные сведения о как OSC кэширует сведения друзей в папке контактов можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="3635c-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="3635c-115">Сведения для каждого друга, возвращаемые в параметре _personsCollection_ стандарту определение схемы XML для **пользователя**.</span><span class="sxs-lookup"><span data-stu-id="3635c-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="3635c-116">Элемент **человека** поддерживает множество элементов данных для каждого друга, если включить адреса электронной почты SMTP (сопоставленных элементов **emailAddress**, **emailAddress2**и **emailAddress3** ) указал, что на friend социальные сети и идентификатор (который сопоставляет элемент **userID** ), идентифицирующий этот friend в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="3635c-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="3635c-117">Чтобы показать действий для пользователей Outlook, выбранного в области пользователей, OSC пытается сопоставить пользователя с каждой friend, возвращенный из **GetFriendsAndColleagues**.</span><span class="sxs-lookup"><span data-stu-id="3635c-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="3635c-118">OSC осуществляется путем сравнения SMTP-адрес выбранного пользователя Outlook с адресами электронной почты, заданные в каждом друге в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="3635c-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="3635c-119">Если OSC находит соответствующий адрес электронной почты SMTP, OSC использует соответствующий **идентификатор пользователя** friend для вызова метода [ISocialSession::GetPerson](isocialsession-getperson.md) .</span><span class="sxs-lookup"><span data-stu-id="3635c-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="3635c-120">Это делается для получения объекта [ISocialPerson](isocialpersoniunknown.md) для этого friend, которое затем позволяет OSC для получения действия и изображений, friend из социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="3635c-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="3635c-121">Тем не менее если на учетную запись в социальных сетях выбранного пользователя Outlook не указана, SMTP-адрес или Outlook пользователь не имеет учетной записи в этой социальной сети, OSC не сможет найти соответствие для этого пользователя и не будет отображаться любой activiti ES для этого пользователя в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="3635c-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3635c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3635c-122">See also</span></span>

- [<span data-ttu-id="3635c-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3635c-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="3635c-124">Получение сведений о друзьях</span><span class="sxs-lookup"><span data-stu-id="3635c-124">Getting Friends Information</span></span>](getting-friends-information.md)

