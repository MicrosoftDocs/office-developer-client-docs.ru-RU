---
title: Работа с большими столбцами
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 11007fa18a57e296472c28f86480cb71b780e568
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593034"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="339fa-103">Работа с большими столбцами</span><span class="sxs-lookup"><span data-stu-id="339fa-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="339fa-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="339fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="339fa-105">Столбцы с данными, свойство строки или двоичный могут занимать много места, много тысяч байтов.</span><span class="sxs-lookup"><span data-stu-id="339fa-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="339fa-106">Так как включить один или несколько столбцов с сотни байт в представлении часто является нецелесообразным, MAPI позволяет разработчику таблице имеющееся значение, чаще всего для 255 байт и реже 510 в байтах.</span><span class="sxs-lookup"><span data-stu-id="339fa-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="339fa-107">По возможности специалистов по внедрению таблица должна включать полное значение свойства в столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="339fa-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="339fa-108">Рекомендуется включать только первые 255 байт.</span><span class="sxs-lookup"><span data-stu-id="339fa-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="339fa-109">Клиенты не могут заранее знаете ли таблицы, которые они используют длинного больших столбцов.</span><span class="sxs-lookup"><span data-stu-id="339fa-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="339fa-110">Они должны предполагает, что столбец представляет усеченных свойство, если длина столбца — 255 или 510 байт.</span><span class="sxs-lookup"><span data-stu-id="339fa-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="339fa-111">При необходимости, клиенты могут напрямую принимать полное значение усеченных столбца из объекта в путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="339fa-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="339fa-112">Построение ограничения со свойствами крупных клиентов следует иметь в виду, что он зависит от таблицы разработчика о том, как эти ограничения эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="339fa-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="339fa-113">Некоторые разработчики таблице разрешить ограничения, построенные с усеченными столбец на основе усеченных размер в то время как другие пользователи основывалось на все значение.</span><span class="sxs-lookup"><span data-stu-id="339fa-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="339fa-114">См. также</span><span class="sxs-lookup"><span data-stu-id="339fa-114">See also</span></span>



[<span data-ttu-id="339fa-115">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="339fa-115">MAPI Tables</span></span>](mapi-tables.md)

