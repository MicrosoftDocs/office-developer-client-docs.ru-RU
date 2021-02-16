---
title: FillBkgnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Определяет цвет, используемый для фона (заливки) шаблона заливки фигуры.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436645"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="0a561-103">FillBkgnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="0a561-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="0a561-104">Определяет цвет, используемый для фона (заливки) шаблона заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="0a561-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a561-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a561-105">Remarks</span></span>

<span data-ttu-id="0a561-106">Чтобы установить цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="0a561-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="0a561-107">Чтобы ввести пользовательский цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="0a561-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="0a561-108">Значением пользовательского цвета является цвет RGB, и RGB(*r, g, b*), а не число, будет показано в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="0a561-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="0a561-109">При работе с числами пользовательские цвета имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="0a561-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="0a561-110">Вы можете установить прозрачность заполнения фона в ячейке FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="0a561-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="0a561-111">Чтобы получить ссылку на ячейку FillBkgnd по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0a561-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a561-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0a561-112">Cell name:</span></span>  <br/> | <span data-ttu-id="0a561-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="0a561-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="0a561-114">Чтобы получить ссылку на ячейку FillBkgnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0a561-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a561-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0a561-115">Section index:</span></span>  <br/> |<span data-ttu-id="0a561-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a561-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0a561-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0a561-117">Row index:</span></span>  <br/> |<span data-ttu-id="0a561-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="0a561-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="0a561-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0a561-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0a561-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="0a561-120">**visFillBkgnd**</span></span> <br/> |
   

