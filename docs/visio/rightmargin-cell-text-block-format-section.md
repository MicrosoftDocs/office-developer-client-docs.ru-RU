---
title: RightMargin Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Определяет расстояние между правой границей текстового блока и текстом, который он содержит. Значение по умолчанию — 0,1 дюйма.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433523"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="179a0-104">RightMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="179a0-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="179a0-105">Определяет расстояние между правой границей текстового блока и текстом, который он содержит.</span><span class="sxs-lookup"><span data-stu-id="179a0-105">Determines the distance between the right border of the text block and the text it contains.</span></span> <span data-ttu-id="179a0-106">Значение по умолчанию — 0,1 дюйма.</span><span class="sxs-lookup"><span data-stu-id="179a0-106">The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="179a0-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="179a0-107">Remarks</span></span>

<span data-ttu-id="179a0-108">Это значение не зависит от масштаба рисования.</span><span class="sxs-lookup"><span data-stu-id="179a0-108">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="179a0-109">Если рисунок масштабировать, правое поле остается тем же.</span><span class="sxs-lookup"><span data-stu-id="179a0-109">If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="179a0-110">Чтобы получить ссылку на ячейку RightMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="179a0-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="179a0-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="179a0-111">Cell name:</span></span>  <br/> | <span data-ttu-id="179a0-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="179a0-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="179a0-113">Чтобы получить ссылку на ячейку RightMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="179a0-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="179a0-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="179a0-114">Section index:</span></span>  <br/> |<span data-ttu-id="179a0-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="179a0-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="179a0-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="179a0-116">Row index:</span></span>  <br/> |<span data-ttu-id="179a0-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="179a0-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="179a0-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="179a0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="179a0-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="179a0-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

