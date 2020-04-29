---
title: Сведения о параметрах защиты от нежелательной почты
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook позволяет пользователям задавать параметры для каждой учетной записи, чтобы защитить учетную запись от спама. Такие параметры защиты от нежелательной почты хранятся в разделе, предназначенном для этой учетной записи в профиле пользователя.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316963"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="a8ee5-104">Сведения о параметрах защиты от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="a8ee5-104">About anti-spam settings</span></span>

<span data-ttu-id="a8ee5-105">Outlook позволяет пользователям задавать параметры для каждой учетной записи, чтобы защитить учетную запись от спама.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="a8ee5-106">Такие параметры защиты от нежелательной почты хранятся в разделе, предназначенном для этой учетной записи в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="a8ee5-107">Используйте свойство [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) , чтобы получить уникальный идентификатор (UID) для раздела в профиле, в котором хранятся параметры пользователя для этой учетной записи, в том числе параметры защиты от нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="a8ee5-108">Используйте следующие свойства для получения параметров защиты от нежелательной почты для учетной записи:</span><span class="sxs-lookup"><span data-stu-id="a8ee5-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="a8ee5-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— указывает список адресов электронной почты и доменов, разделенных точкой с запятой, которые пользователь указал как заблокированные отправители для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="a8ee5-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— задает уровень фильтрации нежелательной почты, который пользователь указал для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="a8ee5-111">В следующей таблице приведены поддерживаемые значения.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="a8ee5-112">Поддерживаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8ee5-112">Supported value</span></span> |<span data-ttu-id="a8ee5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="a8ee5-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="a8ee5-114">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a8ee5-114">None</span></span>  <br/> |<span data-ttu-id="a8ee5-115">Равен</span><span class="sxs-lookup"><span data-stu-id="a8ee5-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="a8ee5-116">Низкий</span><span class="sxs-lookup"><span data-stu-id="a8ee5-116">Low</span></span>  <br/> |<span data-ttu-id="a8ee5-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="a8ee5-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="a8ee5-118">Средние</span><span class="sxs-lookup"><span data-stu-id="a8ee5-118">Medium</span></span>  <br/> |<span data-ttu-id="a8ee5-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="a8ee5-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="a8ee5-120">Высокий</span><span class="sxs-lookup"><span data-stu-id="a8ee5-120">High</span></span>  <br/> |<span data-ttu-id="a8ee5-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a8ee5-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="a8ee5-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— указывает список адресов электронной почты и доменов, разделенных точкой с запятой, которые пользователь указал как доверенных получателей для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="a8ee5-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— указывает список адресов электронной почты и доменов, разделенных точкой с запятой, которые пользователь указал как доверенные отправители для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8ee5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a8ee5-124">See also</span></span>

- [<span data-ttu-id="a8ee5-125">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="a8ee5-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="a8ee5-126">Добавление имен в списки фильтров нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="a8ee5-126">Add names to the Junk Email Filter lists</span></span>](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

