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
description: Определяет цвет, используемый для переднего плана (хода) шаблона заливки теней формы.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422252"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="16541-103">ShdwForegnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="16541-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="16541-104">Определяет цвет, используемый для переднего плана (хода) шаблона заливки теней формы.</span><span class="sxs-lookup"><span data-stu-id="16541-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16541-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="16541-105">Remarks</span></span>

<span data-ttu-id="16541-106">Чтобы установить цвет, введите число от 0 до 23, которое является индексом в коллекцию цветов.</span><span class="sxs-lookup"><span data-stu-id="16541-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="16541-107">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="16541-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="16541-108">Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b),* а не номер будет показан в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="16541-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="16541-109">Пользовательские цвета, используемые в числовом режиме, имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="16541-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="16541-110">В ячейке ShdwForegndTrans можно задать прозрачность цвета переднего плана шаблона теневого заполнения фигуры.</span><span class="sxs-lookup"><span data-stu-id="16541-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="16541-111">Чтобы получить ссылку на ячейку ShdwForegnd по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="16541-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16541-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="16541-112">Cell name:</span></span>  <br/> | <span data-ttu-id="16541-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="16541-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="16541-114">Чтобы получить ссылку на ячейку ShdwForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="16541-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16541-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="16541-115">Section index:</span></span>  <br/> |<span data-ttu-id="16541-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16541-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16541-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="16541-117">Row index:</span></span>  <br/> |<span data-ttu-id="16541-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="16541-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="16541-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="16541-119">Cell index:</span></span>  <br/> |<span data-ttu-id="16541-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="16541-120">**visFillShdwForegnd**</span></span> <br/> |
   

