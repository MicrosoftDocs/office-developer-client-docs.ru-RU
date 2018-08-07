---
title: Ячейка Color (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Определяет цвет, используемый для текста фигуры.
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813384"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="f3103-103">Ячейка Color (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="f3103-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="f3103-104">Определяет цвет, используемый для текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="f3103-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3103-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3103-105">Remarks</span></span>

<span data-ttu-id="f3103-106">Чтобы задать цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="f3103-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="f3103-107">Чтобы ввести другой цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="f3103-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="f3103-108">Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="f3103-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="f3103-109">При использовании в операции, настраиваемые цвета имеют значения из 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="f3103-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="f3103-110">Можно задать прозрачность цвет текста в ячейку прозрачность.</span><span class="sxs-lookup"><span data-stu-id="f3103-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="f3103-111">Для получения ссылки на ячейки цвет по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f3103-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3103-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="f3103-112">Cell name:</span></span>  <br/> |<span data-ttu-id="f3103-113">Char.Color [ *i* ] где *i* = < 1 > 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="f3103-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="f3103-114">Для получения ссылки на ячейки цвет по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="f3103-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3103-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f3103-115">Section index:</span></span>  <br/> |<span data-ttu-id="f3103-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="f3103-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="f3103-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f3103-117">Row index:</span></span>  <br/> |<span data-ttu-id="f3103-118">**visRowCharacter** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="f3103-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="f3103-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f3103-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f3103-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="f3103-120">**visCharacterColor**</span></span> <br/> |
   

