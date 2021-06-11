---
title: SortKey Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Номер, определяя порядок действий, которые отображаются в меню ярлыков или тегов действий.
ms.openlocfilehash: d4eb98055f199f603003b068dca9fa7b4e377e52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419662"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="07da7-103">SortKey Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="07da7-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="07da7-104">Номер, определяя порядок действий, которые отображаются в меню ярлыков или тегов действий.</span><span class="sxs-lookup"><span data-stu-id="07da7-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="07da7-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="07da7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07da7-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="07da7-106">Remarks</span></span>

<span data-ttu-id="07da7-107">Действия в теге действия или меню ярлыка отображаются в меню, отсортировали от самого низкого до самого высокого, а в верхней части меню отображаются более низкие числа.</span><span class="sxs-lookup"><span data-stu-id="07da7-107">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu.</span></span> <span data-ttu-id="07da7-108">Если два ряда действий имеют одно и то же значение ячейки SortKey, порядок определяется физическим порядком строки.</span><span class="sxs-lookup"><span data-stu-id="07da7-108">If two action rows have the same SortKey cell value, the order is determined by physical row order.</span></span> <span data-ttu-id="07da7-109">По умолчанию значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="07da7-109">The default is 0 (zero).</span></span>
  
<span data-ttu-id="07da7-110">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="07da7-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07da7-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="07da7-111">Cell name:</span></span>  <br/> |<span data-ttu-id="07da7-112">Действия.</span><span class="sxs-lookup"><span data-stu-id="07da7-112">Actions.</span></span> <span data-ttu-id="07da7-113">*имя*  . SortKeywhere Actions.</span><span class="sxs-lookup"><span data-stu-id="07da7-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="07da7-114">*имя*  — это имя строки Действия</span><span class="sxs-lookup"><span data-stu-id="07da7-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="07da7-115">Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="07da7-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07da7-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="07da7-116">Section index:</span></span>  <br/> |<span data-ttu-id="07da7-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="07da7-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="07da7-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="07da7-118">Row index:</span></span>  <br/> |<span data-ttu-id="07da7-119">**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="07da7-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="07da7-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="07da7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="07da7-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="07da7-121">**visActionSortKey**</span></span> <br/> |
   

