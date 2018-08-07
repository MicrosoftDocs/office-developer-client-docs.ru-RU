---
title: Ячейка LinePattern (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Определяет шаблон линии фигуры. Значение, введенное в ячейку LinePattern — это число, которое является индексом в коллекции шаблонов линии.
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814085"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="25c61-104">Ячейка LinePattern (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="25c61-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="25c61-105">Определяет шаблон линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="25c61-105">Determines the line pattern of the shape.</span></span> <span data-ttu-id="25c61-106">Значение, введенное в ячейку LinePattern — это число, которое является индексом в коллекции шаблонов линии.</span><span class="sxs-lookup"><span data-stu-id="25c61-106">The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="25c61-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="25c61-107">**Value**</span></span>|<span data-ttu-id="25c61-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="25c61-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25c61-109">0</span><span class="sxs-lookup"><span data-stu-id="25c61-109">0</span></span>  <br/> |<span data-ttu-id="25c61-110">Не шаблон линии</span><span class="sxs-lookup"><span data-stu-id="25c61-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="25c61-111">1</span><span class="sxs-lookup"><span data-stu-id="25c61-111">1</span></span>  <br/> |<span data-ttu-id="25c61-112">Solid</span><span class="sxs-lookup"><span data-stu-id="25c61-112">Solid</span></span>  <br/> |
|<span data-ttu-id="25c61-113">2 - 23</span><span class="sxs-lookup"><span data-stu-id="25c61-113">2 - 23</span></span>  <br/> |<span data-ttu-id="25c61-114">В этой строке шаблонов</span><span class="sxs-lookup"><span data-stu-id="25c61-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25c61-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="25c61-115">Remarks</span></span>

<span data-ttu-id="25c61-116">Можно просмотреть семейства шаблон строки в поле **строка** (на вкладке **Главная** в группе **фигуру** щелкните **строку**, выберите пункт **тире**и нажмите кнопку **Другие линии**).</span><span class="sxs-lookup"><span data-stu-id="25c61-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="25c61-117">Чтобы указать пользовательский шаблон, используйте функцию использования в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="25c61-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="25c61-118">Чтобы получить ссылку на ячейку LinePattern по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="25c61-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25c61-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="25c61-119">Cell name:</span></span>  <br/> |<span data-ttu-id="25c61-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="25c61-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="25c61-121">Чтобы получить ссылку на ячейку LinePattern по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="25c61-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25c61-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="25c61-122">Section index:</span></span>  <br/> |<span data-ttu-id="25c61-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="25c61-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="25c61-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="25c61-124">Row index:</span></span>  <br/> |<span data-ttu-id="25c61-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="25c61-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="25c61-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="25c61-126">Cell index:</span></span>  <br/> |<span data-ttu-id="25c61-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="25c61-127">**visLinePattern**</span></span> <br/> |
   

