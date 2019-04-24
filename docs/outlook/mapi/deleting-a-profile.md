---
title: Удаление профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316830"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="aff82-103">Удаление профиля</span><span class="sxs-lookup"><span data-stu-id="aff82-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="aff82-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aff82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="aff82-105">**Удаление профиля**</span><span class="sxs-lookup"><span data-stu-id="aff82-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="aff82-106">Call [ипрофадмин::D елетепрофиле](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="aff82-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="aff82-107">**Делетепрофиле** помечает профиль для удаления, если он используется в данный момент, дождитесь, пока он не станет активным.</span><span class="sxs-lookup"><span data-stu-id="aff82-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="aff82-108">В действительности профиль не исчезает, пока не будет отключен каждый клиент с активным сеансом.</span><span class="sxs-lookup"><span data-stu-id="aff82-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="aff82-109">**Делетепрофиле** вызывает функцию точки входа каждой службы сообщений в профиле с параметром _улконтекст_ , равным мсг_сервице_делете.</span><span class="sxs-lookup"><span data-stu-id="aff82-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="aff82-110">Вызовы функций точки входа происходят до того, как службы физически удаляются из профиля.</span><span class="sxs-lookup"><span data-stu-id="aff82-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

