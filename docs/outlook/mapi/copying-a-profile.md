---
title: Копирование профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424730"
---
# <a name="copying-a-profile"></a><span data-ttu-id="ebce3-103">Копирование профиля</span><span class="sxs-lookup"><span data-stu-id="ebce3-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="ebce3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebce3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebce3-105">Один из способов создания профиля — копирование из существующего профиля и изменение необходимых служб сообщений и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="ebce3-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="ebce3-106">Копирование профиля включает использование объекта администрирования профиля, предоставленного MAPI с помощью [функции MAPIAdminProfiles.](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="ebce3-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="ebce3-107">**Копирование профиля**</span><span class="sxs-lookup"><span data-stu-id="ebce3-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="ebce3-108">Вызовите **MAPIAdminProfiles,** чтобы получить указатель интерфейса **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="ebce3-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="ebce3-109">Вызовите [IProfAdmin::GetProfileTable,](iprofadmin-getprofiletable.md) чтобы получить доступ к таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="ebce3-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="ebce3-110">Создайте ограничение свойств со структурой [SPropertyRestriction,](spropertyrestriction.md) **чтобы** соответствовать PR_DISPLAY_NAME ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)с именем профиля, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="ebce3-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="ebce3-111">Вызовите [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти соответствующую строку в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="ebce3-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="ebce3-112">Вызовите [IProfAdmin::CopyProfile,](iprofadmin-copyprofile.md)передав значение столбца **PR_DISPLAY_NAME** в качестве параметра _lpszOldProfileName._</span><span class="sxs-lookup"><span data-stu-id="ebce3-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

