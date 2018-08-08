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
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808185"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="9c64d-103">Копирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="9c64d-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="9c64d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c64d-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="9c64d-105">**Чтобы скопировать службы сообщений в профиль**</span><span class="sxs-lookup"><span data-stu-id="9c64d-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="9c64d-106">Вызов [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="9c64d-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="9c64d-107">При копировании службы сообщений нового экземпляра службы настроена в точно так же, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="9c64d-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="9c64d-108">В некоторых случаях **CopyMsgService** возвращает ошибку MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="9c64d-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="9c64d-109">Самой распространенной причиной этой ошибки прибыли — это служба сообщение, которое не позволяет так, чтобы быть дублируются.</span><span class="sxs-lookup"><span data-stu-id="9c64d-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

