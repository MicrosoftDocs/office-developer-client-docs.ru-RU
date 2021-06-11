---
title: Свойства форм для ирисовки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412921"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="5d25f-103">Свойства форм для ирисовки</span><span class="sxs-lookup"><span data-stu-id="5d25f-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="5d25f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d25f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d25f-105">Чтобы выдать запрос, значимый для настраиваемого типа сообщений, приложению необходимо знать свойства, которые ожидаются в этом сообщении.</span><span class="sxs-lookup"><span data-stu-id="5d25f-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="5d25f-106">Чтобы получить список свойств, которые использует настраиваемый класс сообщений, клиентская заявка запрашивает диспетчер форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="5d25f-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="5d25f-107">Руководитель формы получает эти сведения из соответствующего файла конфигурации формы, чтобы клиентские приложения могли использовать эту информацию без накладных расходов на активацию самого сервера формы.</span><span class="sxs-lookup"><span data-stu-id="5d25f-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="5d25f-108">Для этого клиентская заявка вызывает [метод IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5d25f-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="5d25f-109">Обратите внимание, что третьим аргументом **resolveMessageClass** является папка, содержаная связанную таблицу контента, которую запрос будет искать для серверов форм.</span><span class="sxs-lookup"><span data-stu-id="5d25f-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="5d25f-110">NULL указывает, что диспетчер форм должен искать все доступные контейнеры форм.</span><span class="sxs-lookup"><span data-stu-id="5d25f-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="5d25f-111">Если запрос должен работать с определенной папкой, лучше включить соответствующий [указатель IMAPIFolder](imapifolderimapicontainer.md) вместо этого.</span><span class="sxs-lookup"><span data-stu-id="5d25f-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d25f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="5d25f-112">See also</span></span>



[<span data-ttu-id="5d25f-113">Взаимодействие с сервером форм</span><span class="sxs-lookup"><span data-stu-id="5d25f-113">Form Server Interactions</span></span>](form-server-interactions.md)

