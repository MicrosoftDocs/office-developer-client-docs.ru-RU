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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420950"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="eba53-103">Инициализация служебных программ MAPI</span><span class="sxs-lookup"><span data-stu-id="eba53-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="eba53-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eba53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eba53-105">Если необходимо использовать только те служебные программы MAPI, которые необходимы, это программы, а также интерфейсы и функции, объявляемые в МАПИУТИЛ MAPI. H-файл заголовков, например **ипропдата** и **итабледата** , не требуется вызывать **мапиинитиализе** для инициализации.</span><span class="sxs-lookup"><span data-stu-id="eba53-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="eba53-106">Дополнительные сведения см. в статье [ипропдата: IMAPIProp](ipropdataimapiprop.md), [итабледата: IUnknown](itabledataiunknown.md)и [мапиинитиализе](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="eba53-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="eba53-107">Вместо этого вызовите функцию **сЦинитмапиутил** .</span><span class="sxs-lookup"><span data-stu-id="eba53-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="eba53-108">Дополнительные сведения см. в разделе [сЦинитмапиутил](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="eba53-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="eba53-109">**СЦинитмапиутил** позволяет клиентским приложениям использовать служебные функции и методы, требующие распределения MAPI, но не запрашивают их явным образом.</span><span class="sxs-lookup"><span data-stu-id="eba53-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="eba53-110">В момент завершения работы выполните вызов **деинитмапиутил** , чтобы освободить ресурсы, подключенные к служебным программам.</span><span class="sxs-lookup"><span data-stu-id="eba53-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="eba53-111">Не вызывайте **мапиунинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="eba53-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="eba53-112">Дополнительные сведения см. в статье [деинитмапиутил](deinitmapiutil.md) and [мапиунинитиализе](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="eba53-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="eba53-113">Обратите внимание на то, что интерфейс **итабледата** не поддерживает табличные уведомления для клиентов, которые вызвали **сЦинитмапиутил** , а не **мапиинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="eba53-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

