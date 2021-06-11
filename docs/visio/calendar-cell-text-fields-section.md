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
description: Определяет календарь, используемый для текстового поля, когда тип данных — Дата.
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424757"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="e7679-103">Calendar Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="e7679-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="e7679-104">Определяет календарь, используемый для текстового поля, когда тип данных — Дата.</span><span class="sxs-lookup"><span data-stu-id="e7679-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7679-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e7679-105">Remarks</span></span>

<span data-ttu-id="e7679-106">Возможные значения: 0 (западный), 1 (арабский хиджри), 2 (еврейский лунный), 3 (тайваньский календарь), 4 (японский император Царствование), 5 (тайский буддист), 6 (корейский данки), 7 (сакская эра), 8 (английский транслитерированный) и 9 (французский транслитерированный).</span><span class="sxs-lookup"><span data-stu-id="e7679-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="e7679-107">Чтобы получить ссылку на ячейку Calendar по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e7679-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7679-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e7679-108">Cell name:</span></span>  <br/> | <span data-ttu-id="e7679-109">*Fields.Calendar[i]* где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e7679-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e7679-110">Чтобы получить ссылку на ячейку Calendar по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e7679-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7679-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e7679-111">Section index:</span></span>  <br/> |<span data-ttu-id="e7679-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="e7679-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="e7679-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e7679-113">Row index:</span></span>  <br/> |<span data-ttu-id="e7679-114">**visRowField**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="e7679-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e7679-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e7679-115">Cell index:</span></span>  <br/> |<span data-ttu-id="e7679-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="e7679-116">**visFieldCalendar**</span></span> <br/> |
   

