---
title: Calendar Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Определяет календарь, используемый для текстового поля, когда тип данных — Date.
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337501"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="784f5-103">Calendar Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="784f5-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="784f5-104">Определяет календарь, используемый для текстового поля, когда тип данных — Date.</span><span class="sxs-lookup"><span data-stu-id="784f5-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="784f5-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="784f5-105">Remarks</span></span>

<span data-ttu-id="784f5-106">Возможные значения: 0 (Западный), 1 (арабский Хиджра), 2 (Еврейский лунный), 3 (тайваньский календарь), 4 (японский императоров Реигн), 5 (тайский), 6 (корейский), 7 (на английском языке), 8 (английский), 8 (французский (транслитерация)) и 9 (французский (французский)).</span><span class="sxs-lookup"><span data-stu-id="784f5-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="784f5-107">Чтобы получить ссылку на ячейку календаря по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="784f5-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="784f5-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="784f5-108">Cell name:</span></span>  <br/> | <span data-ttu-id="784f5-109">Fields. Calendar [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="784f5-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="784f5-110">Чтобы получить ссылку на ячейку календаря по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="784f5-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="784f5-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="784f5-111">Section index:</span></span>  <br/> |<span data-ttu-id="784f5-112">**Виссектионтекстфиелд**</span><span class="sxs-lookup"><span data-stu-id="784f5-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="784f5-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="784f5-113">Row index:</span></span>  <br/> |<span data-ttu-id="784f5-114">**висровфиелд** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="784f5-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="784f5-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="784f5-115">Cell index:</span></span>  <br/> |<span data-ttu-id="784f5-116">**Висфиелдкалендар**</span><span class="sxs-lookup"><span data-stu-id="784f5-116">**visFieldCalendar**</span></span> <br/> |
   

