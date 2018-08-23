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
ms.openlocfilehash: a6636b6298fcf565a297ed5df8a885c43c279c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583850"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="d4a35-103">Получение свойств формы</span><span class="sxs-lookup"><span data-stu-id="d4a35-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="d4a35-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4a35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4a35-105">Для отправки запроса, который может применяться к типу настраиваемого сообщения, приложение должно знать свойства, которые должны быть на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="d4a35-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="d4a35-106">Чтобы получить список свойств, которые использует пользовательский класс сообщения, клиентское приложение запрашивает диспетчера формы MAPI.</span><span class="sxs-lookup"><span data-stu-id="d4a35-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="d4a35-107">Диспетчер форм возвращает эту информацию из файла конфигурации соответствующую форму, чтобы клиентские приложения могут использовать эти сведения без затрат активации самого сервера формы.</span><span class="sxs-lookup"><span data-stu-id="d4a35-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="d4a35-108">Для этого клиентское приложение вызывает метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d4a35-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="d4a35-109">Обратите внимание, что третий аргумент **ResolveMessageClass** к папке, содержащей таблицу связанного содержимого, запрос выполняет поиск серверов формы.</span><span class="sxs-lookup"><span data-stu-id="d4a35-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="d4a35-110">Значение NULL означает, что диспетчер форм должна выполнять все доступные формы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="d4a35-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="d4a35-111">Если запрос будет выполняться для определенной папки, рекомендуется включить соответствующую указатель [IMAPIFolder](imapifolderimapicontainer.md) вместо этого.</span><span class="sxs-lookup"><span data-stu-id="d4a35-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4a35-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d4a35-112">See also</span></span>



[<span data-ttu-id="d4a35-113">Взаимодействие серверов форм</span><span class="sxs-lookup"><span data-stu-id="d4a35-113">Form Server Interactions</span></span>](form-server-interactions.md)

