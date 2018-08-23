---
title: Использование служебных программ MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569535"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="c8892-103">Использование служебных программ MAPI</span><span class="sxs-lookup"><span data-stu-id="c8892-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="c8892-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8892-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8892-105">Служебные программы MAPI состоят из таблицы данных и объекты данных свойств и множество функций для поддержки функций Разное.</span><span class="sxs-lookup"><span data-stu-id="c8892-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="c8892-106">Существует возможность клиенту требуются только этих служебных программ и не должны входить в подсистему MAPI для установления соединения с поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="c8892-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="c8892-107">Если ваш клиент умещается в этой категории, вызовите функцию API [ScInitMapiUtil](scinitmapiutil.md) вместо функции [MAPIInitialize](mapiinitialize.md) во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="c8892-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="c8892-108">**ScInitMapiUtil** позволяет клиентам использовать функции служебной программы, требующие выделения пространства MAPI, однако, не запрашивать выделения пространства явным образом.</span><span class="sxs-lookup"><span data-stu-id="c8892-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="c8892-109">Когда это время остановки вызов [DeinitMapiUtil](deinitmapiutil.md) для освобождения ресурсов, а не [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="c8892-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="c8892-110">Клиенты, которые никогда не могут вызывать **MAPIInitialize** не должны вызывать **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="c8892-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="c8892-111">Если уже звонил **ScInitMapiUtil** , а не **MAPIInitialize** и с помощью таблиц **ITableData** способами, а не через методы **IMAPITable** , обратите внимание, уведомления о таблице не будут работать.</span><span class="sxs-lookup"><span data-stu-id="c8892-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="c8892-112">Уведомления о требуется использование библиотек MAPI и [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c8892-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

