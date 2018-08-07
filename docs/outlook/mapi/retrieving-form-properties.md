---
title: Получение свойств формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812155"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="83c5e-103">Получение свойств формы</span><span class="sxs-lookup"><span data-stu-id="83c5e-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="83c5e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83c5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83c5e-105">Для отправки запроса, который может применяться к типу настраиваемого сообщения, приложение должно знать свойства, которые должны быть на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="83c5e-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="83c5e-106">Чтобы получить список свойств, которые использует пользовательский класс сообщения, клиентское приложение запрашивает диспетчера формы MAPI.</span><span class="sxs-lookup"><span data-stu-id="83c5e-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="83c5e-107">Диспетчер форм возвращает эту информацию из файла конфигурации соответствующую форму, чтобы клиентские приложения могут использовать эти сведения без затрат активации самого сервера формы.</span><span class="sxs-lookup"><span data-stu-id="83c5e-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="83c5e-108">Для этого клиентское приложение вызывает метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="83c5e-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="83c5e-109">Обратите внимание, что третий аргумент **ResolveMessageClass** к папке, содержащей таблицу связанного содержимого, запрос выполняет поиск серверов формы.</span><span class="sxs-lookup"><span data-stu-id="83c5e-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="83c5e-110">Значение NULL означает, что диспетчер форм должна выполнять все доступные формы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="83c5e-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="83c5e-111">Если запрос будет выполняться для определенной папки, рекомендуется включить соответствующую указатель [IMAPIFolder](imapifolderimapicontainer.md) вместо этого.</span><span class="sxs-lookup"><span data-stu-id="83c5e-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83c5e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="83c5e-112">See also</span></span>



[<span data-ttu-id="83c5e-113">Взаимодействие серверов форм</span><span class="sxs-lookup"><span data-stu-id="83c5e-113">Form Server Interactions</span></span>](form-server-interactions.md)

