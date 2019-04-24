---
title: LineWeight Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Определяет толщину линии фигуры. Задайте толщину линии, введя число с допустимой единицей измерения.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341813"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="e8eec-104">LineWeight Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="e8eec-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="e8eec-105">Определяет толщину линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="e8eec-105">Determines the line weight of a shape.</span></span> <span data-ttu-id="e8eec-106">Задайте толщину линии, введя число с допустимой единицей измерения.</span><span class="sxs-lookup"><span data-stu-id="e8eec-106">Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8eec-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8eec-107">Remarks</span></span>

<span data-ttu-id="e8eec-108">Кроме того, можно задать значение LineWeight в диалоговом окне **линия** (на вкладке **Главная** , в группе **фигур** , щелкнуть **линия**, выбрать толщину и щелкнуть \*\*\*\* **больше линий**).</span><span class="sxs-lookup"><span data-stu-id="e8eec-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="e8eec-109">Если единица измерения не введена, используется единица измерения для текста, указанного в диалоговом окне " **Параметры Visio** " (перейдите на вкладку " **файл** " и нажмите кнопку " **Параметры**").</span><span class="sxs-lookup"><span data-stu-id="e8eec-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="e8eec-110">Толщина линии не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="e8eec-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="e8eec-111">Если масштаб документа изменяется, то толщина линии остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="e8eec-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="e8eec-112">Чтобы получить ссылку на ячейку LineWeight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e8eec-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8eec-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8eec-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e8eec-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="e8eec-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="e8eec-115">Чтобы получить ссылку на ячейку LineWeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e8eec-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8eec-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e8eec-116">Section index:</span></span>  <br/> |<span data-ttu-id="e8eec-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e8eec-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e8eec-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e8eec-118">Row index:</span></span>  <br/> |<span data-ttu-id="e8eec-119">**Висровлине**</span><span class="sxs-lookup"><span data-stu-id="e8eec-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="e8eec-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8eec-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e8eec-121">**Вислиневеигхт**</span><span class="sxs-lookup"><span data-stu-id="e8eec-121">**visLineWeight**</span></span> <br/> |
   

