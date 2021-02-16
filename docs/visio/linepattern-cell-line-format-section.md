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
description: Определяет шаблон линии фигуры. Значение, введенного в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416757"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="93093-104">LinePattern Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="93093-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="93093-105">Определяет шаблон линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="93093-105">Determines the line pattern of the shape.</span></span> <span data-ttu-id="93093-106">Значение, введенного в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.</span><span class="sxs-lookup"><span data-stu-id="93093-106">The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="93093-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="93093-107">**Value**</span></span>|<span data-ttu-id="93093-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93093-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="93093-109">0</span><span class="sxs-lookup"><span data-stu-id="93093-109">0</span></span>  <br/> |<span data-ttu-id="93093-110">Без шаблона строки</span><span class="sxs-lookup"><span data-stu-id="93093-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="93093-111">1 </span><span class="sxs-lookup"><span data-stu-id="93093-111">1</span></span>  <br/> |<span data-ttu-id="93093-112">Сплошная</span><span class="sxs-lookup"><span data-stu-id="93093-112">Solid</span></span>  <br/> |
|<span data-ttu-id="93093-113">2 - 23</span><span class="sxs-lookup"><span data-stu-id="93093-113">2 - 23</span></span>  <br/> |<span data-ttu-id="93093-114">Различные шаблоны строк</span><span class="sxs-lookup"><span data-stu-id="93093-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93093-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="93093-115">Remarks</span></span>

<span data-ttu-id="93093-116">Вы можете просмотреть коллекцию шаблонов линий в  диалоговом  окне **"Линия"** (на вкладке "Главная" в группе "Фигура" щелкните **"Линия",**"На пунктиры" и "Дополнительные **строки").**</span><span class="sxs-lookup"><span data-stu-id="93093-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="93093-117">Чтобы указать пользовательский шаблон строки, используйте функцию USE в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="93093-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="93093-118">Чтобы получить ссылку на ячейку LinePattern по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="93093-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93093-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="93093-119">Cell name:</span></span>  <br/> |<span data-ttu-id="93093-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="93093-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="93093-121">Чтобы получить ссылку на ячейку LinePattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="93093-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93093-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="93093-122">Section index:</span></span>  <br/> |<span data-ttu-id="93093-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="93093-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="93093-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="93093-124">Row index:</span></span>  <br/> |<span data-ttu-id="93093-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="93093-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="93093-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="93093-126">Cell index:</span></span>  <br/> |<span data-ttu-id="93093-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="93093-127">**visLinePattern**</span></span> <br/> |
   

