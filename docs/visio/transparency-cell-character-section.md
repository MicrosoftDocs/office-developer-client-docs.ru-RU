---
title: Transparency Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Определяет уровень прозрачности для диапазона цвета текста фигуры.
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280985"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="9f9f5-103">Transparency Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="9f9f5-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="9f9f5-104">Определяет уровень прозрачности для диапазона цвета текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="9f9f5-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="9f9f5-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9f9f5-105">**Value**</span></span>|<span data-ttu-id="9f9f5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f9f5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f9f5-107">0-100</span><span class="sxs-lookup"><span data-stu-id="9f9f5-107">0 - 100</span></span>  <br/> |<span data-ttu-id="9f9f5-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="9f9f5-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="9f9f5-109">Значение по умолчанию: 0% (полностью непрозрачно).</span><span class="sxs-lookup"><span data-stu-id="9f9f5-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f9f5-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="9f9f5-110">Remarks</span></span>

<span data-ttu-id="9f9f5-111">Значения округляются до ближайшей половины процентов.</span><span class="sxs-lookup"><span data-stu-id="9f9f5-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="9f9f5-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="9f9f5-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="9f9f5-113">Несмотря на то, что фигура с полностью прозрачным текстом отображается на странице рисунка как фигура без текста, она взаимодействует с другими объектами на странице точно так же, как если бы ее прозрачность была равна 0%.</span><span class="sxs-lookup"><span data-stu-id="9f9f5-113">Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="9f9f5-114">Вы также можете задать это значение с помощью ползунка на вкладке **Шрифт** в диалоговом окне **текст** (на вкладке **Главная** щелкните стрелку **Шрифт** ).</span><span class="sxs-lookup"><span data-stu-id="9f9f5-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="9f9f5-115">Если раздел символы содержит несколько строк, ячейка прозрачности содержит сведения о форматировании, примененные к поддиапазону текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="9f9f5-115">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text.</span></span> <span data-ttu-id="9f9f5-116">В противном случае он содержит сведения о форматировании для всего текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="9f9f5-116">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="9f9f5-117">Чтобы получить ссылку на ячейку прозрачности по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="9f9f5-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f9f5-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9f9f5-118">Cell name:</span></span>  <br/> |<span data-ttu-id="9f9f5-119">Char. Колортранс [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9f9f5-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9f9f5-120">Чтобы получить ссылку на ячейку "прозрачность" по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9f9f5-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f9f5-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9f9f5-121">Section index:</span></span>  <br/> |<span data-ttu-id="9f9f5-122">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="9f9f5-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="9f9f5-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9f9f5-123">Row index:</span></span>  <br/> |<span data-ttu-id="9f9f5-124">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9f9f5-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9f9f5-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9f9f5-125">Cell index:</span></span>  <br/> |<span data-ttu-id="9f9f5-126">**Висчарактерколортранс**</span><span class="sxs-lookup"><span data-stu-id="9f9f5-126">**visCharacterColorTrans**</span></span> <br/> |
   

