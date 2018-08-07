---
title: Ячейка Font (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Представляет номер шрифта, используемого для форматирования текста. Номера шрифтов зависят шрифты, установленные в системе. Значение 0 указывает на шрифта по умолчанию, обычно Arial.
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813787"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="0629b-105">Ячейка Font (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="0629b-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="0629b-106">Представляет номер шрифта, используемого для форматирования текста.</span><span class="sxs-lookup"><span data-stu-id="0629b-106">Represents the number of the font used to format the text.</span></span> <span data-ttu-id="0629b-107">Номера шрифтов зависят шрифты, установленные в системе.</span><span class="sxs-lookup"><span data-stu-id="0629b-107">Font numbers vary according to the fonts installed on your system.</span></span> <span data-ttu-id="0629b-108">Значение 0 указывает на шрифта по умолчанию, обычно Arial.</span><span class="sxs-lookup"><span data-stu-id="0629b-108">The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0629b-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="0629b-109">Remarks</span></span>

<span data-ttu-id="0629b-110">Для получения ссылки на ячейки шрифта по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0629b-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0629b-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0629b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="0629b-112">Char.Font [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0629b-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0629b-113">Для получения ссылки на ячейки шрифта по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0629b-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0629b-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0629b-114">Section index:</span></span>  <br/> |<span data-ttu-id="0629b-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="0629b-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="0629b-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0629b-116">Row index:</span></span>  <br/> |<span data-ttu-id="0629b-117">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0629b-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0629b-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0629b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="0629b-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="0629b-119">**visCharacterFont**</span></span> <br/> |
   

