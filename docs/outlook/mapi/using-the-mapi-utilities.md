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
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329633"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="7c9e2-103">Использование служебных программ MAPI</span><span class="sxs-lookup"><span data-stu-id="7c9e2-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="7c9e2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c9e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c9e2-105">Служебные программы MAPI состоят из объектов данных и данных свойств таблиц и различных функций для поддержки различных функций.</span><span class="sxs-lookup"><span data-stu-id="7c9e2-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="7c9e2-106">Клиенту может потребоваться использовать только эти служебные программы и не нужно выполнять вход в подсистему MAPI для установления подключения к поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="7c9e2-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="7c9e2-107">Если ваш клиент соответствует этой категории, вызовите функцию API [сЦинитмапиутил](scinitmapiutil.md) , а не функцию [мапиинитиализе](mapiinitialize.md) во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="7c9e2-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="7c9e2-108">**СЦинитмапиутил** позволяет клиентам использовать служебные функции, требующие распределителя MAPI, но не запрашивают явный механизм распределителяй.</span><span class="sxs-lookup"><span data-stu-id="7c9e2-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="7c9e2-109">Когда закрывается время, вызовите [деинитмапиутил](deinitmapiutil.md) для освобождения ресурсов, а не [мапиунинитиализе](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="7c9e2-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="7c9e2-110">Клиенты, которые никогда не вызывают **мапиинитиализе** , не должны вызывать **мапиунинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="7c9e2-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="7c9e2-111">Если вы вызвали **сЦинитмапиутил** , а не **мапиинитиализе** и используете таблицы с помощью \*\*\*\* методов, а не через методы **IMAPITable** , имейте в виду, что уведомления таблицы не будут работать.</span><span class="sxs-lookup"><span data-stu-id="7c9e2-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="7c9e2-112">Для уведомлений требуется использование библиотек MAPI и [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7c9e2-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

