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
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567673"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="3af02-103">Инициализация служебных программ MAPI</span><span class="sxs-lookup"><span data-stu-id="3af02-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="3af02-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3af02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3af02-105">Если только часть MAPI, которые необходимы для использования являются служебных программ, интерфейсы и функции, объявленные в MAPIUTIL MAPI's. Файл заголовка **IPropData** и **ITableData** — необходимо вызвать **MAPIInitialize** для инициализации.</span><span class="sxs-lookup"><span data-stu-id="3af02-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="3af02-106">Дополнительные сведения можно [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)и [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="3af02-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="3af02-107">Вместо этого вызовите функцию **ScInitMapiUtil** .</span><span class="sxs-lookup"><span data-stu-id="3af02-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="3af02-108">Для получения дополнительных сведений см [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="3af02-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="3af02-109">**ScInitMapiUtil** позволяет клиентским приложениям использовать вспомогательные функции и методы, требующие выделения пространства MAPI, однако, не запрашивать их явным образом.</span><span class="sxs-lookup"><span data-stu-id="3af02-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="3af02-110">Во время завершения вызова с **DeinitMapiUtil** для освобождения ресурсов, подключенных к служебных программ.</span><span class="sxs-lookup"><span data-stu-id="3af02-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="3af02-111">Не вызывайте **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="3af02-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="3af02-112">Для получения дополнительных сведений см [DeinitMapiUtil](deinitmapiutil.md) и [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="3af02-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="3af02-113">Обратите внимание, что интерфейс **ITableData** не поддерживает уведомления о таблице для клиентов, которые вызвали **ScInitMapiUtil** , а не **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="3af02-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

