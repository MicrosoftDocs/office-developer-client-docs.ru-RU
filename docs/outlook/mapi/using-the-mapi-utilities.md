---
title: Использование утилит MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409988"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="784ab-103">Использование утилит MAPI</span><span class="sxs-lookup"><span data-stu-id="784ab-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="784ab-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="784ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="784ab-105">Утилиты MAPI состоит из объектов данных таблицы и данных свойств и различных функций для поддержки различных функций.</span><span class="sxs-lookup"><span data-stu-id="784ab-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="784ab-106">Клиент может нуждаться только в этих утилитах и не должен войти в подсистему MAPI, чтобы установить связь с поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="784ab-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="784ab-107">Если клиент подходит к этой категории, позвоните в функцию API [ScInitMapiUtil,](scinitmapiutil.md) а не на [функцию MAPIInitialize](mapiinitialize.md) во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="784ab-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="784ab-108">**ScInitMapiUtil** позволяет клиентам использовать функции утилиты, для которых требуются аллигаторы MAPI, но которые явно не требуют их.</span><span class="sxs-lookup"><span data-stu-id="784ab-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="784ab-109">Когда пришло время закрыться, позвоните [DeinitMapiUtil,](deinitmapiutil.md) чтобы освободить ресурсы, а [не MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="784ab-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="784ab-110">Клиенты, которые никогда не называют **MAPIInitialize,** не должны вызывать **MAPIUninitialize.**</span><span class="sxs-lookup"><span data-stu-id="784ab-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="784ab-111">Если вы вызвали **ScInitMapiUtil,** а не **MAPIInitialize** и используете таблицы с помощью методов **ITableData,** а не методов **IMAPITable,** знайте, что уведомления таблицы не будут работать.</span><span class="sxs-lookup"><span data-stu-id="784ab-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="784ab-112">Уведомления требуют использования библиотек MAPI и [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="784ab-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

