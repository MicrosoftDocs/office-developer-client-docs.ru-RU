---
title: TextDirection Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Определяет направление символов в текстовом блоке.
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406229"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="86069-103">TextDirection Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="86069-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="86069-104">Определяет направление символов в текстовом блоке.</span><span class="sxs-lookup"><span data-stu-id="86069-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="86069-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="86069-105">**Value**</span></span>|<span data-ttu-id="86069-106">**Направление**</span><span class="sxs-lookup"><span data-stu-id="86069-106">**Direction**</span></span>|<span data-ttu-id="86069-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="86069-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="86069-108">нуль</span><span class="sxs-lookup"><span data-stu-id="86069-108">0</span></span>  <br/> | <span data-ttu-id="86069-109">Горизонтальный</span><span class="sxs-lookup"><span data-stu-id="86069-109">Horizontal</span></span>  <br/> |<span data-ttu-id="86069-110">**висткстблклефтторигхт**</span><span class="sxs-lookup"><span data-stu-id="86069-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="86069-111">1,1</span><span class="sxs-lookup"><span data-stu-id="86069-111">1</span></span>  <br/> | <span data-ttu-id="86069-112">Вертикальный</span><span class="sxs-lookup"><span data-stu-id="86069-112">Vertical</span></span>  <br/> |<span data-ttu-id="86069-113">**висткстблктоптоботтом**</span><span class="sxs-lookup"><span data-stu-id="86069-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86069-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="86069-114">Remarks</span></span>

<span data-ttu-id="86069-115">В Office версии 5,0 на японском языке значение этой ячейки было сохранено в ячейке Вертикалтекст в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="86069-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="86069-116">Чтобы получить ссылку на ячейку TextDirection по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="86069-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86069-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="86069-117">Cell name:</span></span>  <br/> | <span data-ttu-id="86069-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="86069-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="86069-119">Чтобы получить ссылку на ячейку TextDirection по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="86069-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86069-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="86069-120">Section index:</span></span>  <br/> |<span data-ttu-id="86069-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="86069-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="86069-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="86069-122">Row index:</span></span>  <br/> |<span data-ttu-id="86069-123">**висровтекст**</span><span class="sxs-lookup"><span data-stu-id="86069-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="86069-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="86069-124">Cell index:</span></span>  <br/> |<span data-ttu-id="86069-125">**висткстблкдиректион**</span><span class="sxs-lookup"><span data-stu-id="86069-125">**visTxtBlkDirection**</span></span> <br/> |
   

