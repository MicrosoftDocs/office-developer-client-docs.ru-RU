---
title: BulletFont Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Представляет число шрифта, используемого для формата текста при указании настраиваемой строки пули, а значение в ячейке Bullet не нулевое.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438465"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="8c3d8-103">BulletFont Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="8c3d8-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="8c3d8-104">Представляет число шрифта, используемого для формата текста при указании настраиваемой строки пули, а значение в ячейке Bullet не нулевое.</span><span class="sxs-lookup"><span data-stu-id="8c3d8-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8c3d8-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c3d8-105">Remarks</span></span>

<span data-ttu-id="8c3d8-106">Номера шрифтов различаются в зависимости от шрифтов, установленных в системе.</span><span class="sxs-lookup"><span data-stu-id="8c3d8-106">Font numbers vary according to the fonts installed on your system.</span></span> <span data-ttu-id="8c3d8-107">Если значение 0 и есть настраиваемая строка пули, используемый шрифт является таким же, как шрифт первого символа абзаца.</span><span class="sxs-lookup"><span data-stu-id="8c3d8-107">If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="8c3d8-108">Чтобы получить ссылку на ячейку BulletFont по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="8c3d8-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c3d8-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8c3d8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="8c3d8-110">Para.BulletFont[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8c3d8-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8c3d8-111">Чтобы получить ссылку на ячейку BulletFont по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8c3d8-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c3d8-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8c3d8-112">Section index:</span></span>  <br/> |<span data-ttu-id="8c3d8-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8c3d8-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8c3d8-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8c3d8-114">Row index:</span></span>  <br/> |<span data-ttu-id="8c3d8-115">**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="8c3d8-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8c3d8-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8c3d8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="8c3d8-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="8c3d8-117">**visBulletFont**</span></span> <br/> |
   

