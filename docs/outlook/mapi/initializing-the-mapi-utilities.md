---
title: Инициализация утилит MAPI
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
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="01f1a-103">Инициализация утилит MAPI</span><span class="sxs-lookup"><span data-stu-id="01f1a-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="01f1a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01f1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01f1a-105">Если единственной частью MAPI, которую необходимо использовать, являются утилиты — интерфейсы и функции, объявленные в MAPI MAPI. H заглавной файл, такие как **IPropData** и **ITableData** — вам не нужно вызывать **MAPIInitialize** для инициализации.</span><span class="sxs-lookup"><span data-stu-id="01f1a-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="01f1a-106">Дополнительные сведения см. в [iPropData : IMAPIProp,](ipropdataimapiprop.md) [ITableData : IUnknown](itabledataiunknown.md)и [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="01f1a-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="01f1a-107">Вместо этого позвоните **в функцию ScInitMapiUtil.**</span><span class="sxs-lookup"><span data-stu-id="01f1a-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="01f1a-108">Дополнительные сведения см. [в ст. ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="01f1a-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="01f1a-109">**ScInitMapiUtil** позволяет клиентские приложения использовать полезные функции и методы, для которых требуются аллигаторы MAPI, но которые не требуют их явно.</span><span class="sxs-lookup"><span data-stu-id="01f1a-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="01f1a-110">Во время остановки позвоните **в DeinitMapiUtil,** чтобы освободить ресурсы, подключенные к утилитам.</span><span class="sxs-lookup"><span data-stu-id="01f1a-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="01f1a-111">Не **вызывай MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="01f1a-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="01f1a-112">Дополнительные сведения см. [в deinitMapiUtil](deinitmapiutil.md) и [MAPIUninitialize.](mapiuninitialize.md)</span><span class="sxs-lookup"><span data-stu-id="01f1a-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="01f1a-113">Следует помнить, что интерфейс **ITableData** не поддерживает таблицы уведомлений для клиентов, которые вызвали **ScInitMapiUtil,** а **не MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="01f1a-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

