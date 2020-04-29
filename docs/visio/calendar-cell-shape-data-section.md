---
title: Calendar Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Определяет календарь, используемый для данных фигуры, когда типом данных является "Дата".
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432760"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="d4129-103">Calendar Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="d4129-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="d4129-104">Определяет календарь, используемый для данных фигуры, когда типом данных является "Дата".</span><span class="sxs-lookup"><span data-stu-id="d4129-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4129-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4129-105">Remarks</span></span>

<span data-ttu-id="d4129-106">Возможные значения: 0 (Западный), 1 (арабский Хиджра), 2 (Еврейский лунный), 3 (тайваньский календарь), 4 (японский императоров Реигн), 5 (тайский), 6 (корейский), 7 (на английском языке), 8 (английский), 8 (французский (транслитерация)) и 9 (французский (французский)).</span><span class="sxs-lookup"><span data-stu-id="d4129-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="d4129-107">Чтобы получить ссылку на ячейку календаря по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d4129-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4129-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d4129-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d4129-109">Установите.  *Name (имя* ). Календарь, в котором prop.  *Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="d4129-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d4129-110">Чтобы получить ссылку на ячейку календаря по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d4129-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4129-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d4129-111">Section index:</span></span>  <br/> |<span data-ttu-id="d4129-112">**виссектионпроп**</span><span class="sxs-lookup"><span data-stu-id="d4129-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="d4129-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d4129-113">Row index:</span></span>  <br/> |<span data-ttu-id="d4129-114">**висровпроп** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d4129-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d4129-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d4129-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d4129-116">**вискустпропскалендар**</span><span class="sxs-lookup"><span data-stu-id="d4129-116">**visCustPropsCalendar**</span></span> <br/> |
   

