---
title: Получение и задание значений нескольких свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 150f2a55bff4188c1f692de8276ed869bcf66c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808543"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="74caa-103">Получение и задание значений нескольких свойств</span><span class="sxs-lookup"><span data-stu-id="74caa-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="74caa-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74caa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74caa-105">Получение и установка столько свойств по мере возможности с наименьшим число вызовов удаленного сокращен активности и уменьшается нагрузка с каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="74caa-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="74caa-106">Хотя для поставщиков услуг попробовать собирать свойства перед внесением удаленного вызова процедур для извлечения или изменения, можно оптимизировать этот объем работ, начинается с запрашивающего значений нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="74caa-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="74caa-107">Например при работе с списков маршрутизации, которые описывают будущих получателей с именованными свойствами, относящегося к конкретному свойству наборов процесса всех получателей с два звонка.</span><span class="sxs-lookup"><span data-stu-id="74caa-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="74caa-108">Используйте один вызов [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения идентификаторов для всех получателей свойств и другие вызов [IMAPIProp::GetProps](imapiprop-getprops.md) для извлечения всех значений.</span><span class="sxs-lookup"><span data-stu-id="74caa-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="74caa-109">Альтернатива, вызов **GetIDsFromNames** для каждого получателя, а затем вызвать **GetProps** менее эффективный.</span><span class="sxs-lookup"><span data-stu-id="74caa-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

