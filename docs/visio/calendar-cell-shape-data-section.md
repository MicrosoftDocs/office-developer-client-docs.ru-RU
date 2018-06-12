---
title: Ячейка календарного (раздел данных фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Определяет календарь, который используется для данных фигуры, когда тип данных даты.
ms.openlocfilehash: 502ecd8a028c4c0d9841bbd3e0ed369f73bd6b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813322"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="cb53a-103">Ячейка календарного (раздел данных фигуры)</span><span class="sxs-lookup"><span data-stu-id="cb53a-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="cb53a-104">Определяет календарь, который используется для данных фигуры, когда тип данных даты.</span><span class="sxs-lookup"><span data-stu-id="cb53a-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb53a-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb53a-105">Remarks</span></span>

<span data-ttu-id="cb53a-106">Возможные значения: 0 (западное), 1 (арабский хиджра), 2 (Еврейский лунный), 3 (тайваньский), 4 (японский Мэйдзи Reign), 5 (тайский), 6 (корейский Danki), 7 (эра Сака), (транслитерированный английский) 8 и 9 (Транслитерированный французский).</span><span class="sxs-lookup"><span data-stu-id="cb53a-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="cb53a-107">Для получения ссылки на ячейки календаря по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cb53a-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb53a-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cb53a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="cb53a-109">Свойства.  *имя* . Календарь где свойств.  *имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="cb53a-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="cb53a-110">Для получения ссылки на ячейки календаря по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cb53a-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb53a-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cb53a-111">Section index:</span></span>  <br/> |<span data-ttu-id="cb53a-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="cb53a-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="cb53a-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cb53a-113">Row index:</span></span>  <br/> |<span data-ttu-id="cb53a-114">**visRowProp** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cb53a-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cb53a-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cb53a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="cb53a-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="cb53a-116">**visCustPropsCalendar**</span></span> <br/> |
   

