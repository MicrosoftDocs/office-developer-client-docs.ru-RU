---
title: Font Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Представляет номер шрифта, используемого для форматирования текста. Номера шрифтов зависят от установленных в системе шрифтов. Число 0 представляет шрифт по умолчанию, который обычно составляет Arial.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438668"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="4040a-105">Font Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="4040a-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="4040a-106">Представляет номер шрифта, используемого для форматирования текста.</span><span class="sxs-lookup"><span data-stu-id="4040a-106">Represents the number of the font used to format the text.</span></span> <span data-ttu-id="4040a-107">Номера шрифтов зависят от установленных в системе шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4040a-107">Font numbers vary according to the fonts installed on your system.</span></span> <span data-ttu-id="4040a-108">Число 0 представляет шрифт по умолчанию, который обычно составляет Arial.</span><span class="sxs-lookup"><span data-stu-id="4040a-108">The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4040a-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="4040a-109">Remarks</span></span>

<span data-ttu-id="4040a-110">Чтобы получить ссылку на ячейку Font по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="4040a-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4040a-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4040a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="4040a-112">Char. Font [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4040a-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4040a-113">Чтобы получить ссылку на ячейку Font по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4040a-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4040a-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4040a-114">Section index:</span></span>  <br/> |<span data-ttu-id="4040a-115">**виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="4040a-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="4040a-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4040a-116">Row index:</span></span>  <br/> |<span data-ttu-id="4040a-117">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4040a-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4040a-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4040a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="4040a-119">**висчарактерфонт**</span><span class="sxs-lookup"><span data-stu-id="4040a-119">**visCharacterFont**</span></span> <br/> |
   

