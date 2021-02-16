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
description: Определяет календарь, используемый для данных фигуры, когда типом данных является Date.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432760"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="fdb42-103">Calendar Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="fdb42-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="fdb42-104">Определяет календарь, используемый для данных фигуры, когда типом данных является Date.</span><span class="sxs-lookup"><span data-stu-id="fdb42-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fdb42-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="fdb42-105">Remarks</span></span>

<span data-ttu-id="fdb42-106">Возможные значения: 0 (западное), 1 (арабский Хиджра), 2 (иврит, иврит, Иврит), 3 (тайваньский календарь), 4 (японский посвещенный по-японски), 5 (тайский посказок), 6 (корейский Данки), 7 (Saka Era), 8 (транслитерированный английский язык) и 9 (перелитерированный французский).</span><span class="sxs-lookup"><span data-stu-id="fdb42-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="fdb42-107">Чтобы получить ссылку на ячейку Календаря по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fdb42-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdb42-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fdb42-108">Cell name:</span></span>  <br/> | <span data-ttu-id="fdb42-109">Реквизит.  *name*  . Календарь, в котором есть реквизит.  *name*  — имя строки</span><span class="sxs-lookup"><span data-stu-id="fdb42-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="fdb42-110">Чтобы получить ссылку на ячейку Calendar по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fdb42-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdb42-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fdb42-111">Section index:</span></span>  <br/> |<span data-ttu-id="fdb42-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="fdb42-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="fdb42-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fdb42-113">Row index:</span></span>  <br/> |<span data-ttu-id="fdb42-114">**visRowProp**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fdb42-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fdb42-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fdb42-115">Cell index:</span></span>  <br/> |<span data-ttu-id="fdb42-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="fdb42-116">**visCustPropsCalendar**</span></span> <br/> |
   

