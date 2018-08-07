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
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809903"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="81543-103">MapiSvc.inf: раздел [Службы по умолчанию]</span><span class="sxs-lookup"><span data-stu-id="81543-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="81543-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81543-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81543-105">В разделе **[Службы по умолчанию]** перечислены все службы сообщений, выбранные как службы сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81543-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="81543-106">Эти службы сообщений по умолчанию являются подмножеством службы сообщений, перечисленных в разделе **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="81543-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="81543-107">Если программа настройки профиля создает профиль по умолчанию, службы сообщений в этом разделе устанавливаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="81543-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="81543-108">Операции использовать тот же формат как операции в разделе **[Services]** , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="81543-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="81543-109">**[Службы по умолчанию]**</span><span class="sxs-lookup"><span data-stu-id="81543-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="81543-110">_Имя раздела службы сообщений_ =  _имя службы сообщений_</span><span class="sxs-lookup"><span data-stu-id="81543-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="81543-111">Следующие записи должны быть включены в разделе **[Службы по умолчанию]** для mapisvc.inf, показанные на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="81543-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


