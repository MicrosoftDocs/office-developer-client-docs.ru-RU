---
title: Ячейка FillForegnd (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Определяет цвет, используемый для переднего плана (числу штрихов) узора заливки фигуры.
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813769"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="0a19f-103">Ячейка FillForegnd (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="0a19f-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="0a19f-104">Определяет цвет, используемый для переднего плана (числу штрихов) узора заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="0a19f-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a19f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="0a19f-105">Remarks</span></span>

<span data-ttu-id="0a19f-106">Чтобы задать цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="0a19f-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="0a19f-107">Чтобы ввести другой цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="0a19f-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="0a19f-108">Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="0a19f-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="0a19f-109">При использовании в операции, настраиваемые цвета имеют значения из 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="0a19f-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="0a19f-110">Можно задать Прозрачность заливки переднего плана в ячейке FillForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="0a19f-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="0a19f-111">Чтобы получить ссылку на ячейку FillForegnd по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0a19f-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a19f-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0a19f-112">Cell name:</span></span>  <br/> |<span data-ttu-id="0a19f-113">FillForegnd</span><span class="sxs-lookup"><span data-stu-id="0a19f-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="0a19f-114">Для получения ссылки на ячейки FillForegnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0a19f-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a19f-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0a19f-115">Section index:</span></span>  <br/> |<span data-ttu-id="0a19f-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a19f-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0a19f-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0a19f-117">Row index:</span></span>  <br/> |<span data-ttu-id="0a19f-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="0a19f-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="0a19f-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0a19f-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0a19f-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="0a19f-120">**visFillForegnd**</span></span> <br/> |
   

