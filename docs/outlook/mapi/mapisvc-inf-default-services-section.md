---
title: 'MapiSvc.inf: раздел [Службы по умолчанию]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573147"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="4e3a8-103">MapiSvc.inf: раздел [Службы по умолчанию]</span><span class="sxs-lookup"><span data-stu-id="4e3a8-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="4e3a8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e3a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e3a8-105">В разделе **[Службы по умолчанию]** перечислены все службы сообщений, выбранные как службы сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e3a8-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="4e3a8-106">Эти службы сообщений по умолчанию являются подмножеством службы сообщений, перечисленных в разделе **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="4e3a8-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="4e3a8-107">Если программа настройки профиля создает профиль по умолчанию, службы сообщений в этом разделе устанавливаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="4e3a8-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="4e3a8-108">Операции использовать тот же формат как операции в разделе **[Services]** , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4e3a8-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="4e3a8-109">**[Службы по умолчанию]**</span><span class="sxs-lookup"><span data-stu-id="4e3a8-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="4e3a8-110">_Имя раздела службы сообщений_ =  _имя службы сообщений_</span><span class="sxs-lookup"><span data-stu-id="4e3a8-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="4e3a8-111">Следующие записи должны быть включены в разделе **[Службы по умолчанию]** для mapisvc.inf, показанные на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="4e3a8-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


