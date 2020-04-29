---
title: Настройка профиля по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439816"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="3a7d0-103">Настройка профиля по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3a7d0-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="3a7d0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a7d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a7d0-105">Профиль по умолчанию — это профиль, который используется, если вы не указали его явно в вызове [мапилогонекс](mapilogonex.md), установив флаг MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="3a7d0-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="3a7d0-106">**Установка профиля по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="3a7d0-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="3a7d0-107">Вызовите функцию [мапиадминпрофилес](mapiadminprofiles.md) , чтобы получить указатель интерфейса **ипрофадмин** .</span><span class="sxs-lookup"><span data-stu-id="3a7d0-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="3a7d0-108">Call [ипрофадмин:: SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="3a7d0-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="3a7d0-109">**SetDefaultProfile** задает свойство **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) для нового профиля по умолчанию и удаляет параметр для предыдущего профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a7d0-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

