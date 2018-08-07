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
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812257"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="1c1c8-103">Установка профиля по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1c1c8-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="1c1c8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c1c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c1c8-105">Профиль по умолчанию является профиль, который используется, если не указано явно в вызове [MAPILogonEx](mapilogonex.md), вместо этого установка флага MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="1c1c8-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="1c1c8-106">**Чтобы установить профиль по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="1c1c8-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="1c1c8-107">Вызовите функцию [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="1c1c8-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="1c1c8-108">Вызов [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="1c1c8-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="1c1c8-109">**SetDefaultProfile** задает свойство **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) для нового профиля по умолчанию и удаляет параметр для предыдущих профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c1c8-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

