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
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564936"
---
# <a name="copying-a-profile"></a><span data-ttu-id="733df-103">Копирование профиля</span><span class="sxs-lookup"><span data-stu-id="733df-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="733df-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="733df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="733df-105">— Это один из способов создать профиль для копирования из существующего профиля и измените необходимые сообщения служб и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="733df-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="733df-106">Копирование профиль включает использование объект администрирования профилей, предоставляемые MAPI через функцию [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="733df-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="733df-107">**Чтобы скопировать в профиль**</span><span class="sxs-lookup"><span data-stu-id="733df-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="733df-108">Вызов **MAPIAdminProfiles** для получения указателя интерфейса **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="733df-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="733df-109">Вызов [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) для доступа к таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="733df-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="733df-110">Выполните построение ограничение свойства с [SPropertyRestriction](spropertyrestriction.md) структурой в соответствии с **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем профиля для копирования.</span><span class="sxs-lookup"><span data-stu-id="733df-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="733df-111">Вызовите [IMAPITable::FindRow](imapitable-findrow.md) , чтобы найти соответствующую строку в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="733df-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="733df-112">Вызовите [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), передает значение столбца **PR_DISPLAY_NAME** в качестве параметра _lpszOldProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="733df-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

