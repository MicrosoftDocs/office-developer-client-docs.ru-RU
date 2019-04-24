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
description: Представляет номер шрифта, используемого для форматирования текста, если указана строка настраиваемого маркера, а значение в ячейке маркера не равно нулю.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337557"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="eebef-103">BulletFont Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="eebef-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="eebef-104">Представляет номер шрифта, используемого для форматирования текста, если указана строка настраиваемого маркера, а значение в ячейке маркера не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="eebef-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eebef-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eebef-105">Remarks</span></span>

<span data-ttu-id="eebef-106">Номера шрифтов зависят от установленных в системе шрифтов.</span><span class="sxs-lookup"><span data-stu-id="eebef-106">Font numbers vary according to the fonts installed on your system.</span></span> <span data-ttu-id="eebef-107">Если значение равно 0 и имеется настраиваемая строка маркера, используемый шрифт совпадает с шрифтом первого символа абзаца.</span><span class="sxs-lookup"><span data-stu-id="eebef-107">If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="eebef-108">Чтобы получить ссылку на ячейку BulletFont по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="eebef-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eebef-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="eebef-109">Cell name:</span></span>  <br/> | <span data-ttu-id="eebef-110">Para. BulletFont [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="eebef-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="eebef-111">Чтобы получить ссылку на ячейку BulletFont по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="eebef-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eebef-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="eebef-112">Section index:</span></span>  <br/> |<span data-ttu-id="eebef-113">**Виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="eebef-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="eebef-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="eebef-114">Row index:</span></span>  <br/> |<span data-ttu-id="eebef-115">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="eebef-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="eebef-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="eebef-116">Cell index:</span></span>  <br/> |<span data-ttu-id="eebef-117">**Висбуллетфонт**</span><span class="sxs-lookup"><span data-stu-id="eebef-117">**visBulletFont**</span></span> <br/> |
   

