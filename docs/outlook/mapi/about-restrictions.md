---
title: Сведения об ограничениях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 003655354ecac8e2910b3e6851da32c28ce31cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586457"
---
# <a name="about-restrictions"></a><span data-ttu-id="be3ea-103">Сведения об ограничениях</span><span class="sxs-lookup"><span data-stu-id="be3ea-103">About Restrictions</span></span>

  
  
<span data-ttu-id="be3ea-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be3ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be3ea-105">Ограничение — это способ Ограничьте количество строк в представлении только те строки, значения для столбцов, которые соответствуют определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="be3ea-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="be3ea-106">Существует множество различных возможностей по использованию ограничения с таблицами.</span><span class="sxs-lookup"><span data-stu-id="be3ea-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="be3ea-107">Клиентские приложения могут использовать ограничения, например, для фильтрации содержимого таблицы для сообщений, отправленных определенным пользователем, для поиска строк, которые не поддерживают свойство или задания свойства с определенным значением или следует искать повторяющиеся получателей в пределах Сообщение.</span><span class="sxs-lookup"><span data-stu-id="be3ea-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="be3ea-108">Методы [IMAPITable::Restrict](imapitable-restrict.md) и [IMAPITable::FindRow](imapitable-findrow.md) используются для установки ограничений на таблицу.</span><span class="sxs-lookup"><span data-stu-id="be3ea-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="be3ea-109">**Ограничение** применяется ограничение к таблице без извлечение строк.</span><span class="sxs-lookup"><span data-stu-id="be3ea-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="be3ea-110">Для извлечения только тех строк, которые соответствуют ограничение, следующий вызов [IMAPITable::QueryRows](imapitable-queryrows.md) или аналогичным способом является обязательным.</span><span class="sxs-lookup"><span data-stu-id="be3ea-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="be3ea-111">**FindRow** применяется ограничение и получает первой строки в таблице, которая соответствует критериям.</span><span class="sxs-lookup"><span data-stu-id="be3ea-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="be3ea-112">**FindRow** применяется временные ограничения является существовать только в течение вызова, тогда как **ограничить** применяет постоянное ограничение.</span><span class="sxs-lookup"><span data-stu-id="be3ea-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="be3ea-113">Некоторые клиенты могут создавать ограничение, с помощью столбцов, не в текущем столбце заданные.</span><span class="sxs-lookup"><span data-stu-id="be3ea-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="be3ea-114">Поддержка такого ограничения является необязательной и специалистов по внедрению таблицы, которые поддерживают его добавления значения, особенно для таблиц содержимое.</span><span class="sxs-lookup"><span data-stu-id="be3ea-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="be3ea-115">В таблице специалистов по внедрению, которые не поддерживают может возвращать значение MAPI_E_TOO_COMPLEX из вызова **Restrict** или значение MAPI_E_NOT_FOUND из вызова **метода FindRow** .</span><span class="sxs-lookup"><span data-stu-id="be3ea-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="be3ea-116">Клиенты следует иметь в виду, что даже в том случае, если поставщик поддерживает ограничения для столбцов, отсутствующих в текущий набор столбцов, они получат общую производительность, указав столбцы, которые они должны использовать в своих ограничения с [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="be3ea-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be3ea-117">См. также</span><span class="sxs-lookup"><span data-stu-id="be3ea-117">See also</span></span>



[<span data-ttu-id="be3ea-118">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="be3ea-118">MAPI Tables</span></span>](mapi-tables.md)

