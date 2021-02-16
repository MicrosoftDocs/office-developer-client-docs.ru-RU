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
description: Определяет, формирует ли приложение фигуры на основе внутренней невидимой сетки страницы при настройке макета в диалоговом окне "Настройка макета". (На вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета".)
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424443"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="18508-104">EnableGrid Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="18508-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="18508-105">Определяет, формирует ли приложение фигуры на основе внутренней невидимой сетки страницы  при настройке макета в диалоговом окне "Настройка макета".</span><span class="sxs-lookup"><span data-stu-id="18508-105">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box.</span></span> <span data-ttu-id="18508-106">(На **вкладке "Конструктор"** в группе **"Макет"** щелкните "Страница повторного макета" **и** выберите "Дополнительные **параметры макета".**</span><span class="sxs-lookup"><span data-stu-id="18508-106">(On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="18508-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="18508-107">**Value**</span></span>|<span data-ttu-id="18508-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="18508-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18508-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="18508-109">TRUE</span></span>  <br/> |<span data-ttu-id="18508-110">Используйте внутреннюю сетку страниц.</span><span class="sxs-lookup"><span data-stu-id="18508-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="18508-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="18508-111">FALSE</span></span>  <br/> |<span data-ttu-id="18508-112">Не используйте внутреннюю сетку страниц.</span><span class="sxs-lookup"><span data-stu-id="18508-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18508-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="18508-113">Remarks</span></span>

<span data-ttu-id="18508-114">Сетка страницы создается с помощью пространства  между фигурами и  значений среднего размера фигур в диалоговом окне "Макет" и "Интервал маршрутов". </span><span class="sxs-lookup"><span data-stu-id="18508-114">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="18508-115">(На **вкладке "Конструктор"** щелкните **стрелку** "Настройка страницы", выберите "Макет" и "Маршрут" **и** щелкните **"Интервал".)**</span><span class="sxs-lookup"><span data-stu-id="18508-115">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="18508-116">Когда вы включаете эту функцию, приложение выравнивает каждую центрную точку фигуры с центром блока во внутренней сетке страниц.</span><span class="sxs-lookup"><span data-stu-id="18508-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="18508-117">Чтобы получить ссылку на ячейку EnableGrid по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="18508-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18508-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="18508-118">Cell name:</span></span>  <br/> |<span data-ttu-id="18508-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="18508-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="18508-120">Чтобы получить ссылку на ячейку EnableGrid по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="18508-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18508-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="18508-121">Section index:</span></span>  <br/> |<span data-ttu-id="18508-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18508-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="18508-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="18508-123">Row index:</span></span>  <br/> |<span data-ttu-id="18508-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="18508-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="18508-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="18508-125">Cell index:</span></span>  <br/> |<span data-ttu-id="18508-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="18508-126">**visPLOEnableGrid**</span></span> <br/> |
   

