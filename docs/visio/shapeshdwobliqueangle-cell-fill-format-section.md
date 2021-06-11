---
title: ShapeShdwObliqueAngle Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
localization_priority: Normal
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: Указывает угол наклонного направления тени фигуры.
ms.openlocfilehash: 005415e497a4d985d3fb8ec70d62ba40d9e80c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414034"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a><span data-ttu-id="7e771-103">ShapeShdwObliqueAngle Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="7e771-103">ShapeShdwObliqueAngle Cell (Fill Format Section)</span></span>

<span data-ttu-id="7e771-104">Указывает угол наклонного направления тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="7e771-104">Specifies the angle of oblique direction of a shape's shadow.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e771-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e771-105">Remarks</span></span>

<span data-ttu-id="7e771-106">Значение 0 (0) в этой ячейке указывает, что направление угла прямо вверх и измеряется перемещением по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="7e771-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
<span data-ttu-id="7e771-107">Это значение соответствует значению параметра **Direction** в диалоговом окне **Shadow** (на вкладке **Главная,** в группе **Shape** нажмите кнопку **Тень,** а затем нажмите **параметры Shadow).**</span><span class="sxs-lookup"><span data-stu-id="7e771-107">This value corresponds to the value of the **Direction** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="7e771-108">Чтобы получить ссылку на ячейку ShapeShdwObliqueAngle по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="7e771-108">To get a reference to the ShapeShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e771-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7e771-109">Cell name:</span></span>  <br/> | <span data-ttu-id="7e771-110">ShapeShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="7e771-110">ShapeShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="7e771-111">Чтобы получить ссылку на ячейку ShapeShdwObliqueAngle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7e771-111">To get a reference to the ShapeShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e771-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7e771-112">Section index:</span></span>  <br/> |<span data-ttu-id="7e771-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7e771-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7e771-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7e771-114">Row index:</span></span>  <br/> |<span data-ttu-id="7e771-115">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="7e771-115">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="7e771-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7e771-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7e771-117">**visFillShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="7e771-117">**visFillShdwObliqueAngle**</span></span> <br/> |
   

