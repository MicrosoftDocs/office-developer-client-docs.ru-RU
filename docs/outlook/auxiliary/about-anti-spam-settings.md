---
title: О параметрах защиты от нежелательной почты
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook позволяет пользователям указывать параметры для каждой учетной записи, чтобы обеспечить защиту от нежелательной почты учетной записи. Такие параметры защиты от нежелательной почты, хранятся в раздел для этой учетной записи в профиль пользователя.
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807664"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="436a5-104">О параметрах защиты от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="436a5-104">About anti-spam settings</span></span>

<span data-ttu-id="436a5-105">Outlook позволяет пользователям указывать параметры для каждой учетной записи, чтобы обеспечить защиту от нежелательной почты учетной записи.</span><span class="sxs-lookup"><span data-stu-id="436a5-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="436a5-106">Такие параметры защиты от нежелательной почты, хранятся в раздел для этой учетной записи в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="436a5-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="436a5-107">Свойство [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) используется для получения уникального идентификатора (UID) для того раздела, в профиле, в которой хранятся пользовательские параметры для этой учетной записи, включая параметры защиты от нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="436a5-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="436a5-108">Для получения параметров защиты от нежелательной почты для учетной записи, используйте следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="436a5-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="436a5-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— указывает, разделенных точкой с запятой список адресов электронной почты и доменов, которые пользователь указал как заблокированных отправителей для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="436a5-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="436a5-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— определяет уровень фильтрации нежелательной почты-указанного пользователя для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="436a5-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="436a5-111">В следующей таблице показаны поддерживаемые значения.</span><span class="sxs-lookup"><span data-stu-id="436a5-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="436a5-112">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="436a5-112">Supported value</span></span> |<span data-ttu-id="436a5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="436a5-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="436a5-114">Нет</span><span class="sxs-lookup"><span data-stu-id="436a5-114">None</span></span>  <br/> |<span data-ttu-id="436a5-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="436a5-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="436a5-116">Low</span><span class="sxs-lookup"><span data-stu-id="436a5-116">Low</span></span>  <br/> |<span data-ttu-id="436a5-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="436a5-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="436a5-118">Средний</span><span class="sxs-lookup"><span data-stu-id="436a5-118">Medium</span></span>  <br/> |<span data-ttu-id="436a5-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="436a5-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="436a5-120">High</span><span class="sxs-lookup"><span data-stu-id="436a5-120">High</span></span>  <br/> |<span data-ttu-id="436a5-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="436a5-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="436a5-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— указывает, разделенных точкой с запятой список адресов электронной почты и доменов, которые пользователь указал как надежных получателей для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="436a5-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="436a5-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— указывает, разделенных точками с запятой список адресов электронной почты и доменов, которые пользователь указал в качестве надежных отправителей для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="436a5-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="436a5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="436a5-124">See also</span></span>

- [<span data-ttu-id="436a5-125">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="436a5-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="436a5-126">Добавление имен в списки фильтра нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="436a5-126">Add names to the Junk Email Filter lists</span></span>](http://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

