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
# <a name="color-cell-layers-section"></a><span data-ttu-id="e4879-103">Color Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="e4879-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="e4879-104">Указывает цвет, используемый для отображения слоя.</span><span class="sxs-lookup"><span data-stu-id="e4879-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4879-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4879-105">Remarks</span></span>

<span data-ttu-id="e4879-106">Чтобы установить цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="e4879-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="e4879-107">Это значение ячейки соответствует параметру **цвета Layer** в диалоговом  окне **Свойства** слоя  (в группе редактирования на вкладке **Home** щелкните Слои и нажмите кнопку **Свойства слоя).**</span><span class="sxs-lookup"><span data-stu-id="e4879-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="e4879-108">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="e4879-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="e4879-109">Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b),* а не номер будет показан в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e4879-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="e4879-110">Пользовательские цвета, используемые в числовом режиме, имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="e4879-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="e4879-111">Значение 255 указывает, что слой не имеет цвета.</span><span class="sxs-lookup"><span data-stu-id="e4879-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="e4879-112">Можно установить прозрачность цвета слоя в ячейке Transparency.</span><span class="sxs-lookup"><span data-stu-id="e4879-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="e4879-113">Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e4879-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4879-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e4879-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e4879-115">Layers.Color[i] где *i* = <1>, 2, 3, ... </span><span class="sxs-lookup"><span data-stu-id="e4879-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="e4879-116">Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e4879-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4879-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e4879-117">Section index:</span></span>  <br/> |<span data-ttu-id="e4879-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="e4879-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="e4879-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e4879-119">Row index:</span></span>  <br/> |<span data-ttu-id="e4879-120">**visRowLayer**  +   *i,* *где i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="e4879-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="e4879-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e4879-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e4879-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="e4879-122">**visLayerColor**</span></span> <br/> |
   

