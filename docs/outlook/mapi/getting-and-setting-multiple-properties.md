---
title: Получение и установка нескольких свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432263"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="5ba10-103">Получение и установка нескольких свойств</span><span class="sxs-lookup"><span data-stu-id="5ba10-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="5ba10-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ba10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ba10-105">При получении и установке максимального количества свойств с наименьшим количеством вызовов удаленные действия снижаются, а затраты, связанные с каждым свойством, снижаются.</span><span class="sxs-lookup"><span data-stu-id="5ba10-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="5ba10-106">Хотя поставщики служб пытаются собрать свойства перед вызовом удаленной процедуры для и получения или изменения, вы можете оптимизировать эти усилия, запросив несколько свойств для начала.</span><span class="sxs-lookup"><span data-stu-id="5ba10-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="5ba10-107">Например, если вы работаете со списками маршрутизации, которые описывают будущих получателей с именоваными свойствами, принадлежащими определенным наборам свойств, обработать всех получателей с помощью двух вызовов.</span><span class="sxs-lookup"><span data-stu-id="5ba10-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="5ba10-108">Используйте один вызов [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения идентификаторов всех свойств получателя, а другой вызов [IMAPIProp::GetProps](imapiprop-getprops.md) для получения всех значений.</span><span class="sxs-lookup"><span data-stu-id="5ba10-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="5ba10-109">Альтернатива вызову **GetIDsFromNames** и **вызову GetProps** для каждого получателя гораздо менее эффективна.</span><span class="sxs-lookup"><span data-stu-id="5ba10-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

