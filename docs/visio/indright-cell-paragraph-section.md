---
title: Ячейка IndRight (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Представляет расстояние, на котором все строки абзаца находятся от правого поля блока текста. Это значение не зависит от масштаба документа. Если документа изменяется, отступ справа остается неизменным.
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813957"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="5427a-105">Ячейка IndRight (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="5427a-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="5427a-106">Представляет расстояние, на котором все строки абзаца находятся от правого поля блока текста.</span><span class="sxs-lookup"><span data-stu-id="5427a-106">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block.</span></span> <span data-ttu-id="5427a-107">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="5427a-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="5427a-108">Если документа изменяется, отступ справа остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="5427a-108">If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5427a-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="5427a-109">Remarks</span></span>

<span data-ttu-id="5427a-110">Чтобы получить ссылку на ячейку IndRight по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5427a-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5427a-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5427a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="5427a-112">Para.IndRight [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5427a-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5427a-113">Для получения ссылки на ячейки IndRight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5427a-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5427a-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5427a-114">Section index:</span></span>  <br/> |<span data-ttu-id="5427a-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="5427a-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="5427a-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5427a-116">Row index:</span></span>  <br/> |<span data-ttu-id="5427a-117">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5427a-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5427a-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5427a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="5427a-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="5427a-119">**visIndentRight**</span></span> <br/> |
   

