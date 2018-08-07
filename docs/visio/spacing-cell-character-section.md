---
title: Ячейка Spacing (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Управляет дискового пространства между двумя или более символов. Пространство можно добавляются или удаляются с шагом 1/20 точки.
ms.openlocfilehash: ee714306e22cafb7f6d805851a6f977e93172377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814929"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="c52c1-104">Ячейка Spacing (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="c52c1-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="c52c1-105">Управляет дискового пространства между двумя или более символов.</span><span class="sxs-lookup"><span data-stu-id="c52c1-105">Controls the amount of space between two or more characters.</span></span> <span data-ttu-id="c52c1-106">Пространство можно добавляются или удаляются с шагом 1/20 точки.</span><span class="sxs-lookup"><span data-stu-id="c52c1-106">Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c52c1-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="c52c1-107">Remarks</span></span>

<span data-ttu-id="c52c1-108">Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ).</span><span class="sxs-lookup"><span data-stu-id="c52c1-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="c52c1-109">Для получения ссылки на ячейки интервал по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c52c1-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c52c1-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c52c1-110">Cell name:</span></span>  <br/> |<span data-ttu-id="c52c1-111">Char.Letterspace [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c52c1-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c52c1-112">Для получения ссылки на ячейки интервал по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c52c1-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c52c1-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c52c1-113">Section index:</span></span>  <br/> |<span data-ttu-id="c52c1-114">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="c52c1-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="c52c1-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c52c1-115">Row index:</span></span>  <br/> |<span data-ttu-id="c52c1-116">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c52c1-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c52c1-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c52c1-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c52c1-118">**visCharacterLetterspace**</span><span class="sxs-lookup"><span data-stu-id="c52c1-118">**visCharacterLetterspace**</span></span> <br/> |
   

