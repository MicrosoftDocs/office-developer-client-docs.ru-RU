---
title: Ячейка Color (раздел "Слои")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Определяет цвет, используемый для отображения на уровне.
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813401"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="57747-103">Ячейка Color (раздел "Слои")</span><span class="sxs-lookup"><span data-stu-id="57747-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="57747-104">Определяет цвет, используемый для отображения на уровне.</span><span class="sxs-lookup"><span data-stu-id="57747-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57747-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="57747-105">Remarks</span></span>

<span data-ttu-id="57747-106">Чтобы задать цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="57747-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="57747-107">Это значение ячейки соответствует параметру **цвет слоя** в диалоговом окне **Свойства слоя** (в группе **Правка** на вкладке **Главная** нажмите кнопку **уровни** и выберите пункт **Свойства Layer**).</span><span class="sxs-lookup"><span data-stu-id="57747-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="57747-108">Чтобы ввести другой цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="57747-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="57747-109">Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="57747-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="57747-110">При использовании в операции, настраиваемые цвета имеют значения из 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="57747-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="57747-111">Значение 255 указывает уровень без цвета.</span><span class="sxs-lookup"><span data-stu-id="57747-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="57747-112">Можно задать прозрачность цвет слоя в ячейке прозрачность.</span><span class="sxs-lookup"><span data-stu-id="57747-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="57747-113">Для получения ссылки на ячейки цвет по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="57747-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57747-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="57747-114">Cell name:</span></span>  <br/> |<span data-ttu-id="57747-115">Layers.Color [ *i* ] где *i* = < 1 > 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="57747-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="57747-116">Для получения ссылки на ячейки цвет по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="57747-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57747-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="57747-117">Section index:</span></span>  <br/> |<span data-ttu-id="57747-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="57747-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="57747-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="57747-119">Row index:</span></span>  <br/> |<span data-ttu-id="57747-120">**visRowLayer** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="57747-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="57747-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="57747-121">Cell index:</span></span>  <br/> |<span data-ttu-id="57747-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="57747-122">**visLayerColor**</span></span> <br/> |
   

