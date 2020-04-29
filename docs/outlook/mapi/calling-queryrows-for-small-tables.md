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
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404178"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="a0647-103">Вызов QueryRows для небольших таблиц</span><span class="sxs-lookup"><span data-stu-id="a0647-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="a0647-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0647-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0647-105">При извлечении строк из маленькой таблицы вызывайте функцию [IMAPITable:: QueryRows](imapitable-queryrows.md) , а не создавать ограничение.</span><span class="sxs-lookup"><span data-stu-id="a0647-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="a0647-106">Создание ограничения влияет на производительность, так как поставщик должен сначала создать таблицу, найти подходящие строки в исходной таблице, а затем скопировать строки в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="a0647-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="a0647-107">Если общее количество строк в таблице меньше 100, вероятно, лучше прочитать все строки, а затем вызвать команду [IMAPITable:: FindRow](imapitable-findrow.md) , чтобы найти соответствующую строку.</span><span class="sxs-lookup"><span data-stu-id="a0647-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="a0647-108">Это особенно хорошая стратегия, если эти сведения необходимы только иногда.</span><span class="sxs-lookup"><span data-stu-id="a0647-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="a0647-109">Правильное время использования ограничения заключается в том, что сведения об ограниченных или фильтрованных данных будут использоваться в течение более длительного периода времени или часто используются.</span><span class="sxs-lookup"><span data-stu-id="a0647-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="a0647-110">Например, если вы всегда хотите представление с непрочитанными сообщениями, то следует использовать ограничение.</span><span class="sxs-lookup"><span data-stu-id="a0647-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

