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
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573721"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="2bc6a-103">Копирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="2bc6a-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="2bc6a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bc6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2bc6a-105">**Чтобы скопировать службы сообщений в профиль**</span><span class="sxs-lookup"><span data-stu-id="2bc6a-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="2bc6a-106">Вызов [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="2bc6a-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="2bc6a-107">При копировании службы сообщений нового экземпляра службы настроена в точно так же, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="2bc6a-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="2bc6a-108">В некоторых случаях **CopyMsgService** возвращает ошибку MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="2bc6a-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="2bc6a-109">Самой распространенной причиной этой ошибки прибыли — это служба сообщение, которое не позволяет так, чтобы быть дублируются.</span><span class="sxs-lookup"><span data-stu-id="2bc6a-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

