---
title: Удаление службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808277"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="5c5cf-103">Удаление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="5c5cf-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="5c5cf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c5cf-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="5c5cf-105">**Чтобы удалить службы сообщений из профиля**</span><span class="sxs-lookup"><span data-stu-id="5c5cf-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="5c5cf-106">Вызов **IMAPISession::GetMsgServiceTable** для доступа к таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c5cf-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="5c5cf-107">Найдите строку для службы сообщений и передайте его столбец **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) с помощью параметра _lpuid_ [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="5c5cf-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="5c5cf-108">**DeleteMsgService** вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , равным MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="5c5cf-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="5c5cf-109">Службы сообщений выполните какие-либо очистки задач, в настоящее время перед их удалением из профиля.</span><span class="sxs-lookup"><span data-stu-id="5c5cf-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

