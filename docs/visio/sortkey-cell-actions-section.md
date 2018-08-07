---
title: Ячейка SortKey (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Число, определяющее порядок действий, которые отображаются на действие или контекстное меню тега.
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814939"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="86656-103">Ячейка SortKey (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="86656-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="86656-104">Число, определяющее порядок действий, которые отображаются на действие или контекстное меню тега.</span><span class="sxs-lookup"><span data-stu-id="86656-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="86656-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="86656-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86656-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="86656-106">Remarks</span></span>

<span data-ttu-id="86656-107">Действия на тег или контекстное меню действий отображаются в меню Упорядочить от низшего к наибольшим, с нижней номера отображаются в верхней части меню.</span><span class="sxs-lookup"><span data-stu-id="86656-107">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu.</span></span> <span data-ttu-id="86656-108">Если две строки действие имеют такое же значение ячейки SortKey, порядок определяется порядок физических строк.</span><span class="sxs-lookup"><span data-stu-id="86656-108">If two action rows have the same SortKey cell value, the order is determined by physical row order.</span></span> <span data-ttu-id="86656-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="86656-109">The default is 0 (zero).</span></span>
  
<span data-ttu-id="86656-110">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="86656-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86656-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="86656-111">Cell name:</span></span>  <br/> |<span data-ttu-id="86656-112">Действия.</span><span class="sxs-lookup"><span data-stu-id="86656-112">Actions.</span></span> <span data-ttu-id="86656-113">*имя* . SortKeywhere действия.</span><span class="sxs-lookup"><span data-stu-id="86656-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="86656-114">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="86656-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="86656-115">Для получения ссылки на ячейки SortKey по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="86656-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86656-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="86656-116">Section index:</span></span>  <br/> |<span data-ttu-id="86656-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="86656-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="86656-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="86656-118">Row index:</span></span>  <br/> |<span data-ttu-id="86656-119">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="86656-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="86656-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="86656-120">Cell index:</span></span>  <br/> |<span data-ttu-id="86656-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="86656-121">**visActionSortKey**</span></span> <br/> |
   

