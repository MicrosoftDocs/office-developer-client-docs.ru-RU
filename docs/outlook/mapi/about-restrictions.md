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
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433110"
---
# <a name="about-restrictions"></a><span data-ttu-id="2b501-103">Сведения об ограничениях</span><span class="sxs-lookup"><span data-stu-id="2b501-103">About Restrictions</span></span>

  
  
<span data-ttu-id="2b501-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b501-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b501-105">Ограничение — это способ ограничить количество строк в представлении только теми строками, которые имеют значения для столбцов, соответствующих определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="2b501-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="2b501-106">Существует множество различных возможностей использования ограничений в таблицах.</span><span class="sxs-lookup"><span data-stu-id="2b501-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="2b501-107">Клиентские приложения могут использовать ограничения, например, для фильтрации таблицы содержимого для сообщений, отправленных определенным лицом, для поиска строк, которые не поддерживают свойство или не приводят к определенному значению свойства или для поиска повторяющихся получателей в сообщении.</span><span class="sxs-lookup"><span data-stu-id="2b501-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="2b501-108">Методы [IMAPITable:: restrict](imapitable-restrict.md) и [IMAPITable:: FindRow](imapitable-findrow.md) используются для установки ограничений на таблицу.</span><span class="sxs-lookup"><span data-stu-id="2b501-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="2b501-109">**Restrict** применяет ограничение к таблице без извлечения каких бы то ни было строк.</span><span class="sxs-lookup"><span data-stu-id="2b501-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="2b501-110">Чтобы получить только те строки, которые соответствуют ограничению, последующий вызов метода [IMAPITable:: QueryRows](imapitable-queryrows.md) или аналогичный метод является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2b501-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="2b501-111">**FindRow** применяет ограничение и извлекает из таблицы первую строку, которая соответствует условиям.</span><span class="sxs-lookup"><span data-stu-id="2b501-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="2b501-112">Метод **FindRow** применяет временное ограничение, которое имеет значение только в течение срока действия звонка, в то время как **ограничение** применяет более постоянное ограничение.</span><span class="sxs-lookup"><span data-stu-id="2b501-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="2b501-113">Некоторые клиенты могут создавать ограничения с помощью столбцов, которые не входят в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="2b501-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="2b501-114">Поддержка такого ограничения является необязательной и разработчиками таблиц, которые поддерживают эту возможность, особенно для таблиц содержимого.</span><span class="sxs-lookup"><span data-stu-id="2b501-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="2b501-115">Средства реализации таблиц, которые не поддерживают эту функцию, могут возвращать MAPI_E_TOO_COMPLEX значение из метода **Restricting** или MAPI_E_NOT_FOUNDного значения метода **FindRow** .</span><span class="sxs-lookup"><span data-stu-id="2b501-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="2b501-116">Клиенты должны знать, что даже если поставщик поддерживает ограничения для столбцов, не включенных в текущий набор столбцов, производительность будет больше, если указать столбцы, которые они будут использовать в своих ограничениях, с помощью [IMAPITable:: метода SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="2b501-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b501-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2b501-117">See also</span></span>



[<span data-ttu-id="2b501-118">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="2b501-118">MAPI Tables</span></span>](mapi-tables.md)

