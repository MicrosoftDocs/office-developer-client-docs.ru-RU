---
title: DoubleULine Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Определяет, есть ли в диапазоне текста двойное подчеркивание.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357465"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="fac95-103">DoubleULine Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="fac95-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="fac95-104">Определяет, есть ли в диапазоне текста двойное подчеркивание.</span><span class="sxs-lookup"><span data-stu-id="fac95-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="fac95-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="fac95-105">**Value**</span></span>|<span data-ttu-id="fac95-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fac95-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fac95-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fac95-107">TRUE</span></span>  <br/> |<span data-ttu-id="fac95-108">В тексте под ним находится двойное подчеркивание.</span><span class="sxs-lookup"><span data-stu-id="fac95-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="fac95-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fac95-109">FALSE</span></span>  <br/> |<span data-ttu-id="fac95-110">Под текстом не может быть двойное подчеркивание.</span><span class="sxs-lookup"><span data-stu-id="fac95-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fac95-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="fac95-111">Remarks</span></span>

<span data-ttu-id="fac95-112">Ячейка DoubleULine содержит сведения о форматировании, примененные к поддиапазону текста фигуры, если раздел "символы" содержит несколько строк.</span><span class="sxs-lookup"><span data-stu-id="fac95-112">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows.</span></span> <span data-ttu-id="fac95-113">В противном случае он содержит сведения о форматировании для всего текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="fac95-113">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="fac95-114">Значение этой ячейки также можно задать с помощью диалогового окна **текст** (щелкните стрелку на вкладке **Главная** ). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="fac95-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="fac95-115">Чтобы получить ссылку на ячейку DoubleULine по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fac95-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fac95-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fac95-116">Cell name:</span></span>  <br/> |<span data-ttu-id="fac95-117">Char. Дблундерлине [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fac95-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fac95-118">Чтобы получить ссылку на ячейку DoubleULine по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fac95-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fac95-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fac95-119">Section index:</span></span>  <br/> |<span data-ttu-id="fac95-120">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="fac95-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="fac95-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fac95-121">Row index:</span></span>  <br/> |<span data-ttu-id="fac95-122">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fac95-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fac95-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fac95-123">Cell index:</span></span>  <br/> |<span data-ttu-id="fac95-124">**Висчарактердблундерлине**</span><span class="sxs-lookup"><span data-stu-id="fac95-124">**visCharacterDblUnderline**</span></span> <br/> |
   

