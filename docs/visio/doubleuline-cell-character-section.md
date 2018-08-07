---
title: Ячейка DoubleULine (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Определяет, есть ли диапазон текста двойного подчеркивания под ней.
ms.openlocfilehash: d0a07d8c86bd7e9ed3eb14074dda164f82c92475
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813654"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="d1c77-103">Ячейка DoubleULine (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="d1c77-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="d1c77-104">Определяет, есть ли диапазон текста двойного подчеркивания под ней.</span><span class="sxs-lookup"><span data-stu-id="d1c77-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="d1c77-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d1c77-105">**Value**</span></span>|<span data-ttu-id="d1c77-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1c77-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1c77-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d1c77-107">TRUE</span></span>  <br/> |<span data-ttu-id="d1c77-108">Текст имеет двойное подчеркивание под ней.</span><span class="sxs-lookup"><span data-stu-id="d1c77-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="d1c77-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d1c77-109">FALSE</span></span>  <br/> |<span data-ttu-id="d1c77-110">Текст не имеет двойное подчеркивание под ней.</span><span class="sxs-lookup"><span data-stu-id="d1c77-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1c77-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1c77-111">Remarks</span></span>

<span data-ttu-id="d1c77-112">Ячейка DoubleULine содержит сведения о форматировании применяется поддиапазона текстом фигуры в том случае, если в разделе символов содержит несколько строк.</span><span class="sxs-lookup"><span data-stu-id="d1c77-112">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows.</span></span> <span data-ttu-id="d1c77-113">В противном случае содержит сведения о форматировании для всех текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="d1c77-113">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="d1c77-114">Можно также задать значение ячейки с помощью диалогового окна **текста** (щелкните стрелку **шрифта** на вкладке **Главная** ).</span><span class="sxs-lookup"><span data-stu-id="d1c77-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="d1c77-115">Чтобы получить ссылку на ячейку DoubleULine по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d1c77-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1c77-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d1c77-116">Cell name:</span></span>  <br/> |<span data-ttu-id="d1c77-117">Char.DblUnderline [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d1c77-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d1c77-118">Для получения ссылки на ячейки DoubleULine по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d1c77-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1c77-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d1c77-119">Section index:</span></span>  <br/> |<span data-ttu-id="d1c77-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d1c77-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d1c77-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d1c77-121">Row index:</span></span>  <br/> |<span data-ttu-id="d1c77-122">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d1c77-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d1c77-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d1c77-123">Cell index:</span></span>  <br/> |<span data-ttu-id="d1c77-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="d1c77-124">**visCharacterDblUnderline**</span></span> <br/> |
   

