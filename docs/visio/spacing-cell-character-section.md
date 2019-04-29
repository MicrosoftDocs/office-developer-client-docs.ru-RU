---
title: Spacing Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Управляет расстоянием между двумя или более символами. Место можно добавить или вычесть с шагом 1/20-й точки.
ms.openlocfilehash: 927b6203b81af453411cdd13b6f8c8342507a61b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430065"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="a5a21-104">Spacing Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="a5a21-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="a5a21-105">Управляет расстоянием между двумя или более символами.</span><span class="sxs-lookup"><span data-stu-id="a5a21-105">Controls the amount of space between two or more characters.</span></span> <span data-ttu-id="a5a21-106">Место можно добавить или вычесть с шагом 1/20-й точки.</span><span class="sxs-lookup"><span data-stu-id="a5a21-106">Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5a21-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5a21-107">Remarks</span></span>

<span data-ttu-id="a5a21-108">Значение этой ячейки также можно задать с помощью диалогового окна **текст** (на вкладке **Главная** щелкните значок со стрелкой **шрифта** ).</span><span class="sxs-lookup"><span data-stu-id="a5a21-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="a5a21-109">Чтобы получить ссылку на ячейку интервала по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="a5a21-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5a21-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a5a21-110">Cell name:</span></span>  <br/> |<span data-ttu-id="a5a21-111">Char. Леттерспаце [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a5a21-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a5a21-112">Чтобы получить ссылку на ячейку с интервалом по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a5a21-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5a21-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a5a21-113">Section index:</span></span>  <br/> |<span data-ttu-id="a5a21-114">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="a5a21-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="a5a21-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a5a21-115">Row index:</span></span>  <br/> |<span data-ttu-id="a5a21-116">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a5a21-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a5a21-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a5a21-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a5a21-118">**Висчарактерлеттерспаце**</span><span class="sxs-lookup"><span data-stu-id="a5a21-118">**visCharacterLetterspace**</span></span> <br/> |
   

