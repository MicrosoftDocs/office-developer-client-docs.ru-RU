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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316865"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="d64d8-103">Удаление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="d64d8-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="d64d8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d64d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="d64d8-105">**Удаление службы сообщений из профиля**</span><span class="sxs-lookup"><span data-stu-id="d64d8-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="d64d8-106">Call **IMAPISession:: жетмсгсервицетабле** для доступа к таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d64d8-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="d64d8-107">Откройте строку для службы сообщений и передайте ее столбец **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) в параметре _Лпуид_ в [имсгсервицеадмин::D елетемсгсервице](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="d64d8-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="d64d8-108">**Делетемсгсервице** вызывает функцию точки входа службы сообщений с параметром _улконтекст_ , для которого задано значение мсг_сервице_делете.</span><span class="sxs-lookup"><span data-stu-id="d64d8-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="d64d8-109">Службы сообщений перед удалением из профиля выполняют в данный момент какие – либо задачи по очистке.</span><span class="sxs-lookup"><span data-stu-id="d64d8-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

