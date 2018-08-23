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
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573245"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="ab192-103">Удаление профиля</span><span class="sxs-lookup"><span data-stu-id="ab192-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="ab192-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab192-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ab192-105">**Чтобы удалить профиль**</span><span class="sxs-lookup"><span data-stu-id="ab192-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="ab192-106">Вызов [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="ab192-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="ab192-107">**DeleteProfile** помечает профиля для удаления, если он в настоящее время используется, ждать, пока не является активной удаляет его.</span><span class="sxs-lookup"><span data-stu-id="ab192-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="ab192-108">Профиль не исчезает фактически только после отключения каждого клиента с активного сеанса.</span><span class="sxs-lookup"><span data-stu-id="ab192-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="ab192-109">**DeleteProfile** вызывает функцию точки входа для каждой службы сообщений в профиле совместно с параметром _ulContext_ , равным MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="ab192-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="ab192-110">Вызовы функций точки входа достигаться до служб физически удалены из профиля.</span><span class="sxs-lookup"><span data-stu-id="ab192-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

