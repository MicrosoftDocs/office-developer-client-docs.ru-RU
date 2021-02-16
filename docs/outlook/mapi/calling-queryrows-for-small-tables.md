---
title: Вызов queryRows для небольших таблиц
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404178"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="b37ca-103">Вызов queryRows для небольших таблиц</span><span class="sxs-lookup"><span data-stu-id="b37ca-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="b37ca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b37ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b37ca-105">При искомых строках из небольшой таблицы вызовите [IMAPITable::QueryRows](imapitable-queryrows.md) вместо создания ограничения.</span><span class="sxs-lookup"><span data-stu-id="b37ca-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="b37ca-106">Создание ограничения влияет на производительность, так как поставщик должен сначала создать таблицу, найти совпадающие строки в исходной таблице, а затем скопировать строки в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="b37ca-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="b37ca-107">Если общее число строк в таблице меньше 100, вероятно, эффективнее прочитать все строки и вызвать [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти соответствующую строку.</span><span class="sxs-lookup"><span data-stu-id="b37ca-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="b37ca-108">Это особенно хорошая стратегия, если эта информация требуется только изредка.</span><span class="sxs-lookup"><span data-stu-id="b37ca-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="b37ca-109">Время, необходимое для использования ограничений, — это использование ограниченной или отфильтрованной информации в течение длительного периода времени или частое использование.</span><span class="sxs-lookup"><span data-stu-id="b37ca-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="b37ca-110">Например, если вам всегда требуется представление с непрочитаемыми сообщениями, следует использовать ограничение.</span><span class="sxs-lookup"><span data-stu-id="b37ca-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

