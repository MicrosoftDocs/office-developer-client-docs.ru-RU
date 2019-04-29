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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412249"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="59c5a-104">LineWeight Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="59c5a-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="59c5a-105">Определяет толщину линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="59c5a-105">Determines the line weight of a shape.</span></span> <span data-ttu-id="59c5a-106">Задайте толщину линии, введя число с допустимой единицей измерения.</span><span class="sxs-lookup"><span data-stu-id="59c5a-106">Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59c5a-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="59c5a-107">Remarks</span></span>

<span data-ttu-id="59c5a-108">Кроме того, можно задать значение LineWeight в диалоговом окне **линия** (на вкладке **Главная** , в группе **фигур** , щелкнуть **линия**, выбрать толщину и щелкнуть \*\*\*\* **больше линий**).</span><span class="sxs-lookup"><span data-stu-id="59c5a-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="59c5a-109">Если единица измерения не введена, используется единица измерения для текста, указанного в диалоговом окне " **Параметры Visio** " (перейдите на вкладку " **файл** " и нажмите кнопку " **Параметры**").</span><span class="sxs-lookup"><span data-stu-id="59c5a-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="59c5a-110">Толщина линии не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="59c5a-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="59c5a-111">Если масштаб документа изменяется, то толщина линии остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="59c5a-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="59c5a-112">Чтобы получить ссылку на ячейку LineWeight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="59c5a-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59c5a-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="59c5a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="59c5a-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="59c5a-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="59c5a-115">Чтобы получить ссылку на ячейку LineWeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="59c5a-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59c5a-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="59c5a-116">Section index:</span></span>  <br/> |<span data-ttu-id="59c5a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="59c5a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="59c5a-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="59c5a-118">Row index:</span></span>  <br/> |<span data-ttu-id="59c5a-119">**Висровлине**</span><span class="sxs-lookup"><span data-stu-id="59c5a-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="59c5a-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="59c5a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="59c5a-121">**Вислиневеигхт**</span><span class="sxs-lookup"><span data-stu-id="59c5a-121">**visLineWeight**</span></span> <br/> |
   

