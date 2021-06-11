---
title: FillForegnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Определяет цвет, используемый для переднего плана (хода) шаблона заполнения фигуры.
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415567"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="7053c-103">FillForegnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="7053c-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="7053c-104">Определяет цвет, используемый для переднего плана (хода) шаблона заполнения фигуры.</span><span class="sxs-lookup"><span data-stu-id="7053c-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7053c-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="7053c-105">Remarks</span></span>

<span data-ttu-id="7053c-106">Чтобы установить цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="7053c-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="7053c-107">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="7053c-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="7053c-108">Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b),* а не номер будет показан в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="7053c-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="7053c-109">Пользовательские цвета, используемые в числовом режиме, имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="7053c-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="7053c-110">Вы можете установить прозрачность заполнения переднего плана в ячейке FillForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="7053c-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="7053c-111">Чтобы получить ссылку на ячейку FillForegnd по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="7053c-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7053c-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7053c-112">Cell name:</span></span>  <br/> |<span data-ttu-id="7053c-113">FillForegnd</span><span class="sxs-lookup"><span data-stu-id="7053c-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="7053c-114">Чтобы получить ссылку на ячейку FillForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7053c-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7053c-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7053c-115">Section index:</span></span>  <br/> |<span data-ttu-id="7053c-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7053c-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7053c-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7053c-117">Row index:</span></span>  <br/> |<span data-ttu-id="7053c-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="7053c-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="7053c-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7053c-119">Cell index:</span></span>  <br/> |<span data-ttu-id="7053c-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="7053c-120">**visFillForegnd**</span></span> <br/> |
   

