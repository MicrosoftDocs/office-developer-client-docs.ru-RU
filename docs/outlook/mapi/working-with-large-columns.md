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
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420425"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="a589b-103">Работа с большими столбцами</span><span class="sxs-lookup"><span data-stu-id="a589b-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="a589b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a589b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a589b-105">Столбцы со строковыми или двоичными данными свойств могут быть большими, возможно, большим числом тысяч байт.</span><span class="sxs-lookup"><span data-stu-id="a589b-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="a589b-106">Так как включение одного или нескольких столбцов с сотнями байтов в представление зачастую непрактично, MAPI позволяет разработчикам таблиц усекать значение, чаще всего до 255 байт и менее часто до 510 байт.</span><span class="sxs-lookup"><span data-stu-id="a589b-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="a589b-107">По мере возможности разработчики таблиц должны включать в столбец таблицы полное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a589b-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="a589b-108">Рекомендуемая альтернатива состоит в том, чтобы включить только первые 255 байт.</span><span class="sxs-lookup"><span data-stu-id="a589b-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="a589b-109">Клиенты не могут заранее знать, были ли используемые им таблицы усечены в больших столбцах.</span><span class="sxs-lookup"><span data-stu-id="a589b-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="a589b-110">Следует предполагать, что столбец представляет усеченное свойство, если длина столбца составляет 255 или 510 байт.</span><span class="sxs-lookup"><span data-stu-id="a589b-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="a589b-111">При необходимости клиенты могут напрямую получить полное значение усеченного столбца из объекта, вызвав метод объекта [IMAPIProp::](imapiprop-getprops.md) /PROPS.</span><span class="sxs-lookup"><span data-stu-id="a589b-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="a589b-112">Клиенты, на которых разрабатываются ограничения с использованием больших свойств, должны знать, что это не относится к реализации таблиц.</span><span class="sxs-lookup"><span data-stu-id="a589b-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="a589b-113">Некоторые надстройки таблиц допускают ограничения, которые создаются с усеченным столбцом, на основе усеченного размера, в то время как другие основываются на всем значении.</span><span class="sxs-lookup"><span data-stu-id="a589b-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a589b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a589b-114">See also</span></span>



[<span data-ttu-id="a589b-115">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="a589b-115">MAPI Tables</span></span>](mapi-tables.md)

