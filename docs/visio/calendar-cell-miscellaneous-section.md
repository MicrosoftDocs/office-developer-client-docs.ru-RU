---
title: Calendar Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Определяет календарь, который используется, когда Формула ячейки содержит сведения о дате.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421818"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="1524f-103">Calendar Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="1524f-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="1524f-104">Определяет календарь, который используется, когда Формула ячейки содержит сведения о дате.</span><span class="sxs-lookup"><span data-stu-id="1524f-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1524f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="1524f-105">Remarks</span></span>

<span data-ttu-id="1524f-106">Возможные значения: 0 (Западный), 1 (арабский Хиджра), 2 (Еврейский лунный), 3 (тайваньский календарь), 4 (японский императоров Реигн), 5 (тайский), 6 (корейский), 7 (на английском языке), 8 (английский), 8 (французский (транслитерация)) и 9 (французский (французский)).</span><span class="sxs-lookup"><span data-stu-id="1524f-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="1524f-107">Чтобы получить ссылку на ячейку календаря по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="1524f-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1524f-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1524f-108">Cell name:</span></span>  <br/> | <span data-ttu-id="1524f-109">Календарь</span><span class="sxs-lookup"><span data-stu-id="1524f-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="1524f-110">Чтобы получить ссылку на ячейку календаря по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1524f-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1524f-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1524f-111">Section index:</span></span>  <br/> |<span data-ttu-id="1524f-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1524f-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1524f-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1524f-113">Row index:</span></span>  <br/> |<span data-ttu-id="1524f-114">**висровмиск**</span><span class="sxs-lookup"><span data-stu-id="1524f-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="1524f-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1524f-115">Cell index:</span></span>  <br/> |<span data-ttu-id="1524f-116">**висобжкалендар**</span><span class="sxs-lookup"><span data-stu-id="1524f-116">**visObjCalendar**</span></span> <br/> |
   

