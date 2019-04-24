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
description: Определяет расстояние между правой границей блока текста и содержащимся в нем текстом. Значение по умолчанию 0,1 дюйма.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326777"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="cb80b-104">RightMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="cb80b-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="cb80b-105">Определяет расстояние между правой границей блока текста и содержащимся в нем текстом.</span><span class="sxs-lookup"><span data-stu-id="cb80b-105">Determines the distance between the right border of the text block and the text it contains.</span></span> <span data-ttu-id="cb80b-106">Значение по умолчанию 0,1 дюйма.</span><span class="sxs-lookup"><span data-stu-id="cb80b-106">The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb80b-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb80b-107">Remarks</span></span>

<span data-ttu-id="cb80b-108">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="cb80b-108">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="cb80b-109">Если масштаб документа изменяется, правое поле остается прежним.</span><span class="sxs-lookup"><span data-stu-id="cb80b-109">If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="cb80b-110">Чтобы получить ссылку на ячейку RightMargin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="cb80b-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb80b-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="cb80b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="cb80b-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="cb80b-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="cb80b-113">Чтобы получить ссылку на ячейку RightMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="cb80b-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb80b-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cb80b-114">Section index:</span></span>  <br/> |<span data-ttu-id="cb80b-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cb80b-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cb80b-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cb80b-116">Row index:</span></span>  <br/> |<span data-ttu-id="cb80b-117">**Висровтекст**</span><span class="sxs-lookup"><span data-stu-id="cb80b-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="cb80b-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cb80b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="cb80b-119">**Висткстблкригхтмаргин**</span><span class="sxs-lookup"><span data-stu-id="cb80b-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

