---
title: LinePattern Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Определяет шаблон линии фигуры. Значение, введенное в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316445"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="b3c90-104">LinePattern Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="b3c90-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="b3c90-105">Определяет шаблон линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="b3c90-105">Determines the line pattern of the shape.</span></span> <span data-ttu-id="b3c90-106">Значение, введенное в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.</span><span class="sxs-lookup"><span data-stu-id="b3c90-106">The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="b3c90-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="b3c90-107">**Value**</span></span>|<span data-ttu-id="b3c90-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3c90-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3c90-109">нуль</span><span class="sxs-lookup"><span data-stu-id="b3c90-109">0</span></span>  <br/> |<span data-ttu-id="b3c90-110">Без шаблона линии</span><span class="sxs-lookup"><span data-stu-id="b3c90-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="b3c90-111">1,1</span><span class="sxs-lookup"><span data-stu-id="b3c90-111">1</span></span>  <br/> |<span data-ttu-id="b3c90-112">Сплошная</span><span class="sxs-lookup"><span data-stu-id="b3c90-112">Solid</span></span>  <br/> |
|<span data-ttu-id="b3c90-113">2-23</span><span class="sxs-lookup"><span data-stu-id="b3c90-113">2 - 23</span></span>  <br/> |<span data-ttu-id="b3c90-114">Шаблоны строк для ассортимента</span><span class="sxs-lookup"><span data-stu-id="b3c90-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3c90-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3c90-115">Remarks</span></span>

<span data-ttu-id="b3c90-116">Вы можете просмотреть коллекцию шаблонов линий в диалоговом окне **линия** (на вкладке **Главная** , в группе **фигура** , щелкните **линия**, выберите штрихи и нажмите \*\*\*\* кнопку **другие линии**).</span><span class="sxs-lookup"><span data-stu-id="b3c90-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="b3c90-117">Чтобы указать настраиваемый шаблон линии, используйте функцию USE в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="b3c90-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="b3c90-118">Чтобы получить ссылку на ячейку LinePattern по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b3c90-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3c90-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3c90-119">Cell name:</span></span>  <br/> |<span data-ttu-id="b3c90-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="b3c90-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="b3c90-121">Чтобы получить ссылку на ячейку LinePattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b3c90-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3c90-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b3c90-122">Section index:</span></span>  <br/> |<span data-ttu-id="b3c90-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3c90-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b3c90-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b3c90-124">Row index:</span></span>  <br/> |<span data-ttu-id="b3c90-125">**Висровлине**</span><span class="sxs-lookup"><span data-stu-id="b3c90-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="b3c90-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3c90-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b3c90-127">**Вислинепаттерн**</span><span class="sxs-lookup"><span data-stu-id="b3c90-127">**visLinePattern**</span></span> <br/> |
   

