---
title: Color Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Указывает цвет, используемый для отображения слоя.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435133"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="39267-103">Color Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="39267-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="39267-104">Указывает цвет, используемый для отображения слоя.</span><span class="sxs-lookup"><span data-stu-id="39267-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39267-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="39267-105">Remarks</span></span>

<span data-ttu-id="39267-106">Чтобы задать цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="39267-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="39267-107">Значение ячейки соответствует параметру **Color (цвет** ) в диалоговом окне **Свойства слоя** (в группе **Правка** на вкладке **Главная** щелкните **слои** , а затем выберите **Свойства слоя**).</span><span class="sxs-lookup"><span data-stu-id="39267-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="39267-108">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="39267-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="39267-109">Значение настраиваемого цвета — это цвет RGB, а RGB ( *r, g, b*), а не число, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="39267-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="39267-110">При использовании в числовых операциях дополнительные цвета имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="39267-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="39267-111">Значение 255 указывает на то, что слой не имеет цвета.</span><span class="sxs-lookup"><span data-stu-id="39267-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="39267-112">Можно задать прозрачность цвета слоя в ячейке прозрачности.</span><span class="sxs-lookup"><span data-stu-id="39267-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="39267-113">Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="39267-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39267-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="39267-114">Cell name:</span></span>  <br/> |<span data-ttu-id="39267-115">Слои. Color [ *i* ], где *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="39267-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="39267-116">Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="39267-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39267-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="39267-117">Section index:</span></span>  <br/> |<span data-ttu-id="39267-118">**Виссектионлайер**</span><span class="sxs-lookup"><span data-stu-id="39267-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="39267-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="39267-119">Row index:</span></span>  <br/> |<span data-ttu-id="39267-120">**висровлайер** +  *i* , где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="39267-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="39267-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="39267-121">Cell index:</span></span>  <br/> |<span data-ttu-id="39267-122">**Вислайерколор**</span><span class="sxs-lookup"><span data-stu-id="39267-122">**visLayerColor**</span></span> <br/> |
   

