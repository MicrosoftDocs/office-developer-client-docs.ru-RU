---
title: Ячейка IndLeft (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Представляет расстояние, на котором все строки абзаца находятся от левого поля блока текста. Это значение не зависит от масштаба документа. Если документа изменяется, отступ слева остается неизменным.
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813955"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="312dd-105">Ячейка IndLeft (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="312dd-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="312dd-106">Представляет расстояние, на котором все строки абзаца находятся от левого поля блока текста.</span><span class="sxs-lookup"><span data-stu-id="312dd-106">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block.</span></span> <span data-ttu-id="312dd-107">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="312dd-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="312dd-108">Если документа изменяется, отступ слева остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="312dd-108">If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="312dd-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="312dd-109">Remarks</span></span>

<span data-ttu-id="312dd-110">Чтобы получить ссылку на ячейку IndLeft по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="312dd-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="312dd-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="312dd-111">Cell name:</span></span>  <br/> | <span data-ttu-id="312dd-112">Para.IndLeft [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="312dd-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="312dd-113">Для получения ссылки на ячейки IndLeft по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="312dd-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="312dd-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="312dd-114">Section index:</span></span>  <br/> |<span data-ttu-id="312dd-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="312dd-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="312dd-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="312dd-116">Row index:</span></span>  <br/> |<span data-ttu-id="312dd-117">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="312dd-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="312dd-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="312dd-118">Cell index:</span></span>  <br/> |<span data-ttu-id="312dd-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="312dd-119">**visIndentLeft**</span></span> <br/> |
   

