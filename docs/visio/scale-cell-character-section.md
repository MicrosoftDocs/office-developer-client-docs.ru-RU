---
title: Ячейка Scale (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Определяет ширину шрифта. Значение по умолчанию для этой ячейке составляет 100%.
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814725"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="48ca5-104">Ячейка Scale (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="48ca5-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="48ca5-105">Определяет ширину шрифта.</span><span class="sxs-lookup"><span data-stu-id="48ca5-105">Controls the font width.</span></span> <span data-ttu-id="48ca5-106">Значение по умолчанию для этой ячейке составляет 100%.</span><span class="sxs-lookup"><span data-stu-id="48ca5-106">The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48ca5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="48ca5-107">Remarks</span></span>

<span data-ttu-id="48ca5-108">Задайте процентную долю от 1 до 99% для уменьшения ширины шрифта.</span><span class="sxs-lookup"><span data-stu-id="48ca5-108">Set the percentage between 1% and 99% to decrease the font width.</span></span> <span data-ttu-id="48ca5-109">Задайте его от 101% до 600%, чтобы увеличить ширину шрифта.</span><span class="sxs-lookup"><span data-stu-id="48ca5-109">Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="48ca5-110">Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ).</span><span class="sxs-lookup"><span data-stu-id="48ca5-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="48ca5-111">Для получения ссылки на ячейки масштаба по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="48ca5-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48ca5-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="48ca5-112">Cell name:</span></span>  <br/> |<span data-ttu-id="48ca5-113">Char.FontScale [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="48ca5-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="48ca5-114">Для получения ссылки на ячейки масштаба по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="48ca5-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48ca5-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="48ca5-115">Section index:</span></span>  <br/> |<span data-ttu-id="48ca5-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="48ca5-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="48ca5-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="48ca5-117">Row index:</span></span>  <br/> |<span data-ttu-id="48ca5-118">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="48ca5-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="48ca5-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="48ca5-119">Cell index:</span></span>  <br/> |<span data-ttu-id="48ca5-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="48ca5-120">**visCharacterFontScale**</span></span> <br/> |
   

