---
title: Color Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Определяет цвет, используемый для текста фигуры.
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439991"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="09e4a-103">Color Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="09e4a-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="09e4a-104">Определяет цвет, используемый для текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="09e4a-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09e4a-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="09e4a-105">Remarks</span></span>

<span data-ttu-id="09e4a-106">Чтобы задать цвет, введите число от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="09e4a-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="09e4a-107">Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="09e4a-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="09e4a-108">Значение настраиваемого цвета — это цвет RGB, а RGB ( *r, g, b*), а не число, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="09e4a-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="09e4a-109">При использовании в числовых операциях дополнительные цвета имеют значения 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="09e4a-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="09e4a-110">Вы можете задать прозрачность цвета текста в ячейке прозрачности.</span><span class="sxs-lookup"><span data-stu-id="09e4a-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="09e4a-111">Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="09e4a-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09e4a-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="09e4a-112">Cell name:</span></span>  <br/> |<span data-ttu-id="09e4a-113">Char. Color [ *i* ], где *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="09e4a-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="09e4a-114">Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="09e4a-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09e4a-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="09e4a-115">Section index:</span></span>  <br/> |<span data-ttu-id="09e4a-116">**виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="09e4a-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="09e4a-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="09e4a-117">Row index:</span></span>  <br/> |<span data-ttu-id="09e4a-118">**висровчарактер** +  *i* , где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="09e4a-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="09e4a-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="09e4a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="09e4a-120">**висчарактерколор**</span><span class="sxs-lookup"><span data-stu-id="09e4a-120">**visCharacterColor**</span></span> <br/> |
   

