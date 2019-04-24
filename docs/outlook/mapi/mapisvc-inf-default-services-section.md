---
title: MapiSvc. INF [службы по умолчанию] раздел
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270072"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="8ca80-103">MapiSvc. INF [службы по умолчанию] раздел</span><span class="sxs-lookup"><span data-stu-id="8ca80-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="8ca80-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ca80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ca80-105">В разделе **[службы по умолчанию]** перечислены все службы сообщений, выбранные в качестве служб сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ca80-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="8ca80-106">Эти службы сообщений по умолчанию являются подмножеством служб сообщений, перечисленных в разделе **[службы]** .</span><span class="sxs-lookup"><span data-stu-id="8ca80-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="8ca80-107">Когда программа настройки профилей создает профиль по умолчанию, службы сообщений в этом разделе автоматически включаются.</span><span class="sxs-lookup"><span data-stu-id="8ca80-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="8ca80-108">Записи используют тот же формат, что и записи в разделе **[Services]** , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="8ca80-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="8ca80-109">**[Службы по умолчанию]**</span><span class="sxs-lookup"><span data-stu-id="8ca80-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="8ca80-110">_имя раздела "_ =  служба сообщений" имя_службы сообщений_</span><span class="sxs-lookup"><span data-stu-id="8ca80-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="8ca80-111">Следующие записи будут включены в раздел **[службы по умолчанию]** для файла Mapisvc. INF, показанного на предыдущем рисунке:</span><span class="sxs-lookup"><span data-stu-id="8ca80-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


