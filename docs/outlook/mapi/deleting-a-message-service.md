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
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583570"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="5f08f-103">Удаление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="5f08f-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="5f08f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f08f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5f08f-105">**Чтобы удалить службы сообщений из профиля**</span><span class="sxs-lookup"><span data-stu-id="5f08f-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="5f08f-106">Вызов **IMAPISession::GetMsgServiceTable** для доступа к таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5f08f-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="5f08f-107">Найдите строку для службы сообщений и передайте его столбец **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) с помощью параметра _lpuid_ [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="5f08f-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="5f08f-108">**DeleteMsgService** вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , равным MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="5f08f-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="5f08f-109">Службы сообщений выполните какие-либо очистки задач, в настоящее время перед их удалением из профиля.</span><span class="sxs-lookup"><span data-stu-id="5f08f-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

