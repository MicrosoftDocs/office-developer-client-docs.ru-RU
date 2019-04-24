---
title: Копирование службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333056"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="8fef5-103">Копирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="8fef5-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="8fef5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fef5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8fef5-105">**Копирование службы сообщений в профиль**</span><span class="sxs-lookup"><span data-stu-id="8fef5-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="8fef5-106">Call [имсгсервицеадмин:: копимсгсервице](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="8fef5-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="8fef5-107">При копировании службы сообщений новый экземпляр службы настраивается точно так же, как и в исходном.</span><span class="sxs-lookup"><span data-stu-id="8fef5-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="8fef5-108">Иногда **копимсгсервице** ВОЗВРАЩАЕТ ошибку мапи_е_акцесс_дениед.</span><span class="sxs-lookup"><span data-stu-id="8fef5-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="8fef5-109">Наиболее распространенной причиной этого возврата ошибки является служба сообщений, которая не допускает дублирования.</span><span class="sxs-lookup"><span data-stu-id="8fef5-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

