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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299379"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="53bbc-103">Получение и установка нескольких свойств</span><span class="sxs-lookup"><span data-stu-id="53bbc-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="53bbc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53bbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53bbc-105">Получив и устанавливая как можно больше свойств с наименьшим количеством вызовов, удаленная активность — куртаилед, а нагрузка, связанная с каждым свойством, уменьшается.</span><span class="sxs-lookup"><span data-stu-id="53bbc-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="53bbc-106">Несмотря на то, что поставщики услуг пытаются собрать свойства перед выполнением удаленных вызовов процедур для получения или изменения, можно оптимизировать эту работу, запросив несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="53bbc-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="53bbc-107">Например, при работе со списками маршрутизации, в которых описаны будущие получатели с именованными свойствами, принадлежащими определенным наборам свойств, необходимо обработать всех получателей с двумя вызовами.</span><span class="sxs-lookup"><span data-stu-id="53bbc-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="53bbc-108">Используйте один вызов [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить идентификаторы для всех свойств получателей и другой вызов [IMAPIProp:: Prop](imapiprop-getprops.md) для получения всех значений.</span><span class="sxs-lookup"><span data-stu-id="53bbc-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="53bbc-109">Кроме того, выполнение вызова **жетидсфромнамес** , за которым следует вызов PROPS \*\*\*\* для каждого получателя, гораздо менее эффективно.</span><span class="sxs-lookup"><span data-stu-id="53bbc-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

