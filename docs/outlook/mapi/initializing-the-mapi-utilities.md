---
title: Инициализация utilities MAPI
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
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="e0cbd-103">Инициализация utilities MAPI</span><span class="sxs-lookup"><span data-stu-id="e0cbd-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="e0cbd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0cbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0cbd-105">Если необходимо использовать только программы MAPI, интерфейсы и функции, объявленные в MAPI MAPI MAPI. Файл H-загона, например **IPropData** и **ITableData,** не требуется вызывать **MAPIInitialize** для инициализации.</span><span class="sxs-lookup"><span data-stu-id="e0cbd-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="e0cbd-106">Дополнительные сведения см. в [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)и [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="e0cbd-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="e0cbd-107">Вместо этого вызовите **функцию ScInitMapiUtil.**</span><span class="sxs-lookup"><span data-stu-id="e0cbd-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="e0cbd-108">Дополнительные сведения [см. в подразделе ScInitMapiUtil.](scinitmapiutil.md)</span><span class="sxs-lookup"><span data-stu-id="e0cbd-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="e0cbd-109">**ScInitMapiUtil** позволяет клиентские приложения использовать функции и методы, для которых требуются средства назначения MAPI, но которые не требуют их явно.</span><span class="sxs-lookup"><span data-stu-id="e0cbd-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="e0cbd-110">Во время завершения работы вызовите **DeinitMapiUtil,** чтобы освободить ресурсы, подключенные к средствам.</span><span class="sxs-lookup"><span data-stu-id="e0cbd-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="e0cbd-111">Не **вызывай MAPIUninitialize.**</span><span class="sxs-lookup"><span data-stu-id="e0cbd-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="e0cbd-112">Дополнительные сведения [см. в подразделах DeinitMapiUtil](deinitmapiutil.md) и [MAPIUninitialize.](mapiuninitialize.md)</span><span class="sxs-lookup"><span data-stu-id="e0cbd-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="e0cbd-113">Следует помнить, что интерфейс **ITableData** не поддерживает уведомления таблиц для клиентов, которые вызвали **ScInitMapiUtil,** а **не MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="e0cbd-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

