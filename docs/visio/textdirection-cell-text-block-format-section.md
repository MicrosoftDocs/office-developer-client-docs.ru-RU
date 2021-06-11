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
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="f1213-103">TextDirection Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="f1213-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="f1213-104">Определяет направление символов в текстовом блоке.</span><span class="sxs-lookup"><span data-stu-id="f1213-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="f1213-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f1213-105">**Value**</span></span>|<span data-ttu-id="f1213-106">**Направление**</span><span class="sxs-lookup"><span data-stu-id="f1213-106">**Direction**</span></span>|<span data-ttu-id="f1213-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="f1213-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f1213-108">0</span><span class="sxs-lookup"><span data-stu-id="f1213-108">0</span></span>  <br/> | <span data-ttu-id="f1213-109">Горизонтальный</span><span class="sxs-lookup"><span data-stu-id="f1213-109">Horizontal</span></span>  <br/> |<span data-ttu-id="f1213-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="f1213-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="f1213-111">1</span><span class="sxs-lookup"><span data-stu-id="f1213-111">1</span></span>  <br/> | <span data-ttu-id="f1213-112">Вертикальный</span><span class="sxs-lookup"><span data-stu-id="f1213-112">Vertical</span></span>  <br/> |<span data-ttu-id="f1213-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="f1213-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1213-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1213-114">Remarks</span></span>

<span data-ttu-id="f1213-115">В Visio версии 5.0 японской продукции значение этой ячейки хранилось в ячейке VerticalText в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="f1213-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="f1213-116">Чтобы получить ссылку на ячейку TextDirection по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f1213-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1213-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f1213-117">Cell name:</span></span>  <br/> | <span data-ttu-id="f1213-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="f1213-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="f1213-119">Чтобы получить ссылку на ячейку TextDirection по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f1213-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1213-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f1213-120">Section index:</span></span>  <br/> |<span data-ttu-id="f1213-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f1213-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f1213-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f1213-122">Row index:</span></span>  <br/> |<span data-ttu-id="f1213-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="f1213-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="f1213-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f1213-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f1213-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="f1213-125">**visTxtBlkDirection**</span></span> <br/> |
   

