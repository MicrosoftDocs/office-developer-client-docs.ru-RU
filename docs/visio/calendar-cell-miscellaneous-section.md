---
title: Ячейка Calendar (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Определяет календарь, который будет использоваться при Формула ячейки содержит сведения о дате.
ms.openlocfilehash: 2bca91fd2efc283bcc8f2c5037c4d81dd9bcffc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813312"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="1196f-103">Ячейка Calendar (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="1196f-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="1196f-104">Определяет календарь, который будет использоваться при Формула ячейки содержит сведения о дате.</span><span class="sxs-lookup"><span data-stu-id="1196f-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1196f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1196f-105">Remarks</span></span>

<span data-ttu-id="1196f-106">Возможные значения: 0 (западное), 1 (арабский хиджра), 2 (Еврейский лунный), 3 (тайваньский), 4 (японский Мэйдзи Reign), 5 (тайский), 6 (корейский Danki), 7 (эра Сака), (транслитерированный английский) 8 и 9 (Транслитерированный французский).</span><span class="sxs-lookup"><span data-stu-id="1196f-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="1196f-107">Для получения ссылки на ячейки календаря по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1196f-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1196f-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1196f-108">Cell name:</span></span>  <br/> | <span data-ttu-id="1196f-109">Календарь</span><span class="sxs-lookup"><span data-stu-id="1196f-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="1196f-110">Для получения ссылки на ячейки календаря по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1196f-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1196f-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1196f-111">Section index:</span></span>  <br/> |<span data-ttu-id="1196f-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1196f-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1196f-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1196f-113">Row index:</span></span>  <br/> |<span data-ttu-id="1196f-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="1196f-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="1196f-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1196f-115">Cell index:</span></span>  <br/> |<span data-ttu-id="1196f-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="1196f-116">**visObjCalendar**</span></span> <br/> |
   

