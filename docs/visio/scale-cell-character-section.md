---
title: Scale Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Определяет ширину шрифта. Значение по умолчанию для этой ячейки — 100%.
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341631"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="76b9f-104">Scale Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="76b9f-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="76b9f-105">Определяет ширину шрифта.</span><span class="sxs-lookup"><span data-stu-id="76b9f-105">Controls the font width.</span></span> <span data-ttu-id="76b9f-106">Значение по умолчанию для этой ячейки — 100%.</span><span class="sxs-lookup"><span data-stu-id="76b9f-106">The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76b9f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76b9f-107">Remarks</span></span>

<span data-ttu-id="76b9f-108">Задайте в процентах значение от 1 до 99%, чтобы уменьшить ширину шрифта.</span><span class="sxs-lookup"><span data-stu-id="76b9f-108">Set the percentage between 1% and 99% to decrease the font width.</span></span> <span data-ttu-id="76b9f-109">Задайте для него значение от 101% до 600%, чтобы увеличить ширину шрифта.</span><span class="sxs-lookup"><span data-stu-id="76b9f-109">Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="76b9f-110">Значение этой ячейки также можно задать с помощью диалогового окна **текст** (на вкладке **Главная** щелкните значок со стрелкой **шрифта** ).</span><span class="sxs-lookup"><span data-stu-id="76b9f-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="76b9f-111">Чтобы получить ссылку на ячейку Scale по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="76b9f-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76b9f-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="76b9f-112">Cell name:</span></span>  <br/> |<span data-ttu-id="76b9f-113">Char. Фонтскале [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="76b9f-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="76b9f-114">Чтобы получить ссылку на ячейку Scale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="76b9f-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76b9f-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="76b9f-115">Section index:</span></span>  <br/> |<span data-ttu-id="76b9f-116">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="76b9f-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="76b9f-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="76b9f-117">Row index:</span></span>  <br/> |<span data-ttu-id="76b9f-118">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="76b9f-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="76b9f-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="76b9f-119">Cell index:</span></span>  <br/> |<span data-ttu-id="76b9f-120">**Висчарактерфонтскале**</span><span class="sxs-lookup"><span data-stu-id="76b9f-120">**visCharacterFontScale**</span></span> <br/> |
   

