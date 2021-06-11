---
title: Сведения о параметрах защиты от нежелательной почты
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook позволяет пользователям указывать параметры для каждой учетной записи, чтобы защитить учетную запись от нежелательной почты. Такие параметры для борьбы со спамом хранятся в разделе, назначенном для этой учетной записи в профиле пользователя.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316963"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="ba4fa-104">Сведения о параметрах защиты от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="ba4fa-104">About anti-spam settings</span></span>

<span data-ttu-id="ba4fa-105">Outlook позволяет пользователям указывать параметры для каждой учетной записи, чтобы защитить учетную запись от нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="ba4fa-106">Такие параметры для борьбы со спамом хранятся в разделе, назначенном для этой учетной записи в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="ba4fa-107">Используйте [свойство PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) для получения уникального ID (UID) для раздела в профиле, который хранит предпочтения пользователя для этой учетной записи, включая параметры борьбы со спамом.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="ba4fa-108">Используйте следующие свойства для получения параметров для борьбы со спамом для учетной записи:</span><span class="sxs-lookup"><span data-stu-id="ba4fa-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="ba4fa-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— указывает полуколон-делимитированный список адресов и доменов электронной почты, указанных пользователем в качестве заблокированных отправителей для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="ba4fa-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— указывает уровень фильтрации нежелательной почты, указанный пользователем для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="ba4fa-111">В следующей таблице показаны поддерживаемые значения.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="ba4fa-112">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="ba4fa-112">Supported value</span></span> |<span data-ttu-id="ba4fa-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ba4fa-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="ba4fa-114">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ba4fa-114">None</span></span>  <br/> |<span data-ttu-id="ba4fa-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="ba4fa-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="ba4fa-116">Низкие</span><span class="sxs-lookup"><span data-stu-id="ba4fa-116">Low</span></span>  <br/> |<span data-ttu-id="ba4fa-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="ba4fa-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="ba4fa-118">Средний</span><span class="sxs-lookup"><span data-stu-id="ba4fa-118">Medium</span></span>  <br/> |<span data-ttu-id="ba4fa-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ba4fa-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="ba4fa-120">Фишинговое сообщение с</span><span class="sxs-lookup"><span data-stu-id="ba4fa-120">High</span></span>  <br/> |<span data-ttu-id="ba4fa-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ba4fa-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="ba4fa-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— указывает полуколон-делимитированный список адресов и доменов электронной почты, указанных пользователем в качестве надежных получателей для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="ba4fa-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— указывает полуколон-делимитированный список адресов и доменов электронной почты, указанных пользователем в качестве надежных отправителей для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ba4fa-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba4fa-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ba4fa-124">See also</span></span>

- [<span data-ttu-id="ba4fa-125">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="ba4fa-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="ba4fa-126">Добавление имен в списки фильтра нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="ba4fa-126">Add names to the Junk Email Filter lists</span></span>](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

