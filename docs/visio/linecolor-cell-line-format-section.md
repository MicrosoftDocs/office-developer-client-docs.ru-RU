---
title: LineColor Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Определяет цвет линии фигуры.
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416939"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="e590e-103">LineColor Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="e590e-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="e590e-104">Определяет цвет линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="e590e-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e590e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e590e-105">Remarks</span></span>

<span data-ttu-id="e590e-106">Чтобы установить цвет линии, введите число от 0 до 23, которое является индексом в коллекцию цветов линии.</span><span class="sxs-lookup"><span data-stu-id="e590e-106">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors.</span></span> <span data-ttu-id="e590e-107">Вы можете просмотреть коллекцию цветов линий в  диалоговом окне **"Линия"** (на вкладке "Главная" в группе "Фигура" щелкните **"Строка"** и "Вес" **и** выберите "Дополнительные  **строки").**</span><span class="sxs-lookup"><span data-stu-id="e590e-107">You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span> <span data-ttu-id="e590e-108">Вы также можете установить значение LineColor в **диалоговом** окне "Линия".</span><span class="sxs-lookup"><span data-stu-id="e590e-108">You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="e590e-109">Чтобы ввести пользовательский цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="e590e-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="e590e-110">Значением пользовательского цвета является цвет RGB, и RGB( *r, g, b*), а не число, будет показано в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e590e-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="e590e-111">При работе с числами пользовательские цвета имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="e590e-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="e590e-112">Вы можете установить прозрачность цвета линии в ячейке LineColorTrans.</span><span class="sxs-lookup"><span data-stu-id="e590e-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="e590e-113">Чтобы получить ссылку на ячейку LineColor по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e590e-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e590e-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e590e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e590e-115">LineColor</span><span class="sxs-lookup"><span data-stu-id="e590e-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="e590e-116">Чтобы получить ссылку на ячейку LineColor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e590e-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e590e-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e590e-117">Section index:</span></span>  <br/> |<span data-ttu-id="e590e-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e590e-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e590e-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e590e-119">Row index:</span></span>  <br/> |<span data-ttu-id="e590e-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="e590e-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="e590e-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e590e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e590e-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="e590e-122">**visLineColor**</span></span> <br/> |
   

