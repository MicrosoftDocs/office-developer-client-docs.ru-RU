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
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428125"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="26374-103">Удаление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="26374-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="26374-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="26374-105">**Удаление службы сообщений из профиля**</span><span class="sxs-lookup"><span data-stu-id="26374-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="26374-106">Вызов **IMAPISession::GetMsgServiceTable для** доступа к таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="26374-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="26374-107">Найдите строку для службы сообщений и передайте столбец **PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)в _параметре lpuid_ [службе IMsgServiceAdmin::D eleteMsgService.](imsgserviceadmin-deletemsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="26374-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="26374-108">**DeleteMsgService** вызывает функцию точки входа службы сообщений, для параметра  _ulContext_ установлено MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="26374-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="26374-109">Перед удалением из профиля службы сообщений выполняют все задачи очистки.</span><span class="sxs-lookup"><span data-stu-id="26374-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

