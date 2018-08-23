---
title: Установка профиля по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591774"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="80299-103">Установка профиля по умолчанию</span><span class="sxs-lookup"><span data-stu-id="80299-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="80299-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80299-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80299-105">Профиль по умолчанию является профиль, который используется, если не указано явно в вызове [MAPILogonEx](mapilogonex.md), вместо этого установка флага MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="80299-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="80299-106">**Чтобы установить профиль по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="80299-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="80299-107">Вызовите функцию [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="80299-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="80299-108">Вызов [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="80299-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="80299-109">**SetDefaultProfile** задает свойство **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) для нового профиля по умолчанию и удаляет параметр для предыдущих профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80299-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

