---
title: Вызов QueryRows для небольших таблиц
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589338"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="17590-103">Вызов QueryRows для небольших таблиц</span><span class="sxs-lookup"><span data-stu-id="17590-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="17590-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17590-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17590-105">Во время извлечения строк из небольшая таблица, вызовите [IMAPITable::QueryRows](imapitable-queryrows.md) вместо первого построение ограничение.</span><span class="sxs-lookup"><span data-stu-id="17590-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="17590-106">Создание ограничение влияет на производительность, так как поставщик необходимо сначала создать таблицу, найдите сопоставления строк в исходной таблице и затем скопируйте строки в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="17590-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="17590-107">Если общее число строк в таблице меньше, чем 100, вероятно эффективнее читать все строки, а затем вызвать [IMAPITable::FindRow](imapitable-findrow.md) , чтобы найти соответствующую строку.</span><span class="sxs-lookup"><span data-stu-id="17590-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="17590-108">Это особенно хорошей стратегией, если эти сведения требуются редко.</span><span class="sxs-lookup"><span data-stu-id="17590-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="17590-109">Заданное время для использования с ограничением является ограниченных или отфильтрованные сведения будет использован на длительный период времени или частоты использования.</span><span class="sxs-lookup"><span data-stu-id="17590-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="17590-110">Для экземпляра требуемое всегда представление с непрочитанных сообщений, ограничение — это вызов соответствующих прав для использования.</span><span class="sxs-lookup"><span data-stu-id="17590-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

