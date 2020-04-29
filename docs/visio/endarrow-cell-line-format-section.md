---
title: EndArrow Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Указывает, имеет ли строка наконечник стрелки или другой конечный формат на последней вершине.
ms.openlocfilehash: 54ef11125a8774914a60897850fb75cd4ab949a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434685"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="800f7-103">EndArrow Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="800f7-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="800f7-104">Указывает, имеет ли строка наконечник стрелки или другой конечный формат на последней вершине.</span><span class="sxs-lookup"><span data-stu-id="800f7-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="800f7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="800f7-105">**Value**</span></span>|<span data-ttu-id="800f7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="800f7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="800f7-107">нуль</span><span class="sxs-lookup"><span data-stu-id="800f7-107">0</span></span>  <br/> |<span data-ttu-id="800f7-108">Без наконечника.</span><span class="sxs-lookup"><span data-stu-id="800f7-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="800f7-109">1 - 45</span><span class="sxs-lookup"><span data-stu-id="800f7-109">1 - 45</span></span>  <br/> |<span data-ttu-id="800f7-110">Стили наконечников в ассортименте, которые соответствуют индексированным записям в диалоговом окне " **линия** ".</span><span class="sxs-lookup"><span data-stu-id="800f7-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="800f7-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="800f7-111">Remarks</span></span>

<span data-ttu-id="800f7-112">Вы также можете задать это значение в диалоговом окне **строка** (на вкладке **Главная** , **в группе Группа** , затем последовательно выберите пункты **линия**и **стрелки**и **Другие стрелки**).</span><span class="sxs-lookup"><span data-stu-id="800f7-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="800f7-113">Размер стрелки задается в ячейке EndArrowSize.</span><span class="sxs-lookup"><span data-stu-id="800f7-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="800f7-114">Можно указать настраиваемую строку End с помощью функции USE в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="800f7-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="800f7-115">Чтобы получить ссылку на ячейку EndArrow по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="800f7-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="800f7-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="800f7-116">Cell name:</span></span>  <br/> |<span data-ttu-id="800f7-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="800f7-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="800f7-118">Чтобы получить ссылку на ячейку EndArrow по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="800f7-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="800f7-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="800f7-119">Section index:</span></span>  <br/> |<span data-ttu-id="800f7-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="800f7-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="800f7-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="800f7-121">Row index:</span></span>  <br/> |<span data-ttu-id="800f7-122">**висровлине**</span><span class="sxs-lookup"><span data-stu-id="800f7-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="800f7-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="800f7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="800f7-124">**вислининдарров**</span><span class="sxs-lookup"><span data-stu-id="800f7-124">**visLineEndArrow**</span></span> <br/> |
   

