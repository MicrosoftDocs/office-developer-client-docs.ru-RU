---
title: ShdwForegnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки тени для перепада фигуры.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422252"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="0058f-103">ShdwForegnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="0058f-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="0058f-104">Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки тени для перепада фигуры.</span><span class="sxs-lookup"><span data-stu-id="0058f-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0058f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0058f-105">Remarks</span></span>

<span data-ttu-id="0058f-106">Чтобы установить цвет, введите число от 0 до 23, которое является индексом в коллекцию цветов.</span><span class="sxs-lookup"><span data-stu-id="0058f-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="0058f-107">Чтобы ввести пользовательский цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="0058f-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="0058f-108">Значением пользовательского цвета является цвет RGB, и RGB( *r, g, b*), а не число, будет показано в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="0058f-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="0058f-109">При работе с числами пользовательские цвета имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="0058f-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="0058f-110">Вы можете установить прозрачность цвета переднего плана шаблона заливки теней фигуры в ячейке ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="0058f-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="0058f-111">Чтобы получить ссылку на ячейку ShdwForegnd по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0058f-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0058f-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0058f-112">Cell name:</span></span>  <br/> | <span data-ttu-id="0058f-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="0058f-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="0058f-114">Чтобы получить ссылку на ячейку ShdwForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0058f-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0058f-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0058f-115">Section index:</span></span>  <br/> |<span data-ttu-id="0058f-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0058f-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0058f-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0058f-117">Row index:</span></span>  <br/> |<span data-ttu-id="0058f-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="0058f-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="0058f-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0058f-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0058f-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="0058f-120">**visFillShdwForegnd**</span></span> <br/> |
   

