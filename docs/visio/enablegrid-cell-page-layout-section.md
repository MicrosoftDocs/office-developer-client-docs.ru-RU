---
title: EnableGrid Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Определяет, устанавливает ли приложение фигуры на основе внутренней невидимой сетки страниц при настройке макета в диалоговом окне Configure Layout. (На вкладке Дизайн в группе Макет щелкните страницу Re-Layout и нажмите кнопку Дополнительные параметры макета.)
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424443"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="4063a-104">EnableGrid Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="4063a-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="4063a-105">Определяет, устанавливает ли приложение фигуры на основе внутренней невидимой сетки страниц при настройке макета в диалоговом окне **Configure Layout.**</span><span class="sxs-lookup"><span data-stu-id="4063a-105">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box.</span></span> <span data-ttu-id="4063a-106">(На **вкладке Дизайн** в группе **Макет** щелкните Страницу **повторного** макета и нажмите кнопку **Дополнительные параметры макета.)**</span><span class="sxs-lookup"><span data-stu-id="4063a-106">(On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="4063a-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4063a-107">**Value**</span></span>|<span data-ttu-id="4063a-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4063a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4063a-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="4063a-109">TRUE</span></span>  <br/> |<span data-ttu-id="4063a-110">Используйте внутреннюю сетку страниц.</span><span class="sxs-lookup"><span data-stu-id="4063a-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="4063a-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="4063a-111">FALSE</span></span>  <br/> |<span data-ttu-id="4063a-112">Не используйте внутреннюю сетку страниц.</span><span class="sxs-lookup"><span data-stu-id="4063a-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4063a-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="4063a-113">Remarks</span></span>

<span data-ttu-id="4063a-114">Эта сетка страниц создается с помощью  пространства между фигурами и значениями среднего размера фигуры в диалоговом окне **Макет** и Маршрутная интервал. </span><span class="sxs-lookup"><span data-stu-id="4063a-114">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="4063a-115">(На **вкладке Дизайн** щелкните стрелку **установки** страницы, щелкните **Макет** и маршрутику, а затем щелкните **Интервал**.)</span><span class="sxs-lookup"><span data-stu-id="4063a-115">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="4063a-116">Если включить эту функцию, приложение выравнивает центр каждой фигуры с центром блока на внутренней сетке страницы.</span><span class="sxs-lookup"><span data-stu-id="4063a-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="4063a-117">Чтобы получить ссылку на ячейку EnableGrid по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4063a-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4063a-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4063a-118">Cell name:</span></span>  <br/> |<span data-ttu-id="4063a-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="4063a-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="4063a-120">Чтобы получить ссылку на ячейку EnableGrid по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4063a-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4063a-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4063a-121">Section index:</span></span>  <br/> |<span data-ttu-id="4063a-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4063a-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4063a-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4063a-123">Row index:</span></span>  <br/> |<span data-ttu-id="4063a-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="4063a-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="4063a-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4063a-125">Cell index:</span></span>  <br/> |<span data-ttu-id="4063a-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="4063a-126">**visPLOEnableGrid**</span></span> <br/> |
   

