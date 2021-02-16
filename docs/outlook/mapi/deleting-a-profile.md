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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410205"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="a254b-103">Удаление профиля</span><span class="sxs-lookup"><span data-stu-id="a254b-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="a254b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a254b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a254b-105">**Удаление профиля**</span><span class="sxs-lookup"><span data-stu-id="a254b-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="a254b-106">Вызовите [IProfAdmin::D eleteProfile.](iprofadmin-deleteprofile.md)</span><span class="sxs-lookup"><span data-stu-id="a254b-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="a254b-107">**DeleteProfile** пометит профиль для удаления, если он используется в настоящее время, ожидая, пока он больше не будет активен для удаления.</span><span class="sxs-lookup"><span data-stu-id="a254b-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="a254b-108">Профиль не исчезает до тех пор, пока не будет отключен каждый клиент с активным сеансом.</span><span class="sxs-lookup"><span data-stu-id="a254b-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="a254b-109">**DeleteProfile** вызывает функцию точки входа для каждой службы сообщений в профиле, для параметра  _ulContext_ установлено MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="a254b-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="a254b-110">Вызовы функций точки входа выполняются перед физическим удалением служб из профиля.</span><span class="sxs-lookup"><span data-stu-id="a254b-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

