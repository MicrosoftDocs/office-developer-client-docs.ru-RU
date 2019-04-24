---
title: Инициализация служебных программ MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317222"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="84e2a-103">Инициализация служебных программ MAPI</span><span class="sxs-lookup"><span data-stu-id="84e2a-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="84e2a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84e2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84e2a-105">Если необходимо использовать только те служебные программы MAPI, которые необходимы, это программы, а также интерфейсы и функции, объявляемые в МАПИУТИЛ MAPI. H-файл заголовков, например **ипропдата** и **итабледата** , не требуется вызывать **мапиинитиализе** для инициализации.</span><span class="sxs-lookup"><span data-stu-id="84e2a-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="84e2a-106">Дополнительные сведения см. в статье [ипропдата: IMAPIProp](ipropdataimapiprop.md), [итабледата: IUnknown](itabledataiunknown.md)и [мапиинитиализе](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="84e2a-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="84e2a-107">Вместо этого вызовите функцию **сЦинитмапиутил** .</span><span class="sxs-lookup"><span data-stu-id="84e2a-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="84e2a-108">Дополнительные сведения см. в разделе [сЦинитмапиутил](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="84e2a-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="84e2a-109">**СЦинитмапиутил** позволяет клиентским приложениям использовать служебные функции и методы, требующие распределения MAPI, но не запрашивают их явным образом.</span><span class="sxs-lookup"><span data-stu-id="84e2a-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="84e2a-110">В момент завершения работы выполните вызов **деинитмапиутил** , чтобы освободить ресурсы, подключенные к служебным программам.</span><span class="sxs-lookup"><span data-stu-id="84e2a-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="84e2a-111">Не вызывайте **мапиунинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="84e2a-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="84e2a-112">Дополнительные сведения см. в статье [деинитмапиутил](deinitmapiutil.md) and [мапиунинитиализе](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="84e2a-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="84e2a-113">Обратите внимание на то, что интерфейс **итабледата** не поддерживает табличные уведомления для клиентов, которые вызвали **сЦинитмапиутил** , а не **мапиинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="84e2a-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

