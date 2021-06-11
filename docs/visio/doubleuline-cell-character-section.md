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
description: Определяет, имеет ли диапазон текста двойное подчеркнуть ниже.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438843"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="71047-103">DoubleULine Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="71047-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="71047-104">Определяет, имеет ли диапазон текста двойное подчеркнуть ниже.</span><span class="sxs-lookup"><span data-stu-id="71047-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="71047-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="71047-105">**Value**</span></span>|<span data-ttu-id="71047-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71047-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71047-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="71047-107">TRUE</span></span>  <br/> |<span data-ttu-id="71047-108">Текст имеет двойное подчеркнуть ниже.</span><span class="sxs-lookup"><span data-stu-id="71047-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="71047-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="71047-109">FALSE</span></span>  <br/> |<span data-ttu-id="71047-110">Текст не имеет двойного подчеркнуть ниже.</span><span class="sxs-lookup"><span data-stu-id="71047-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71047-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="71047-111">Remarks</span></span>

<span data-ttu-id="71047-112">Ячейка DoubleULine содержит сведения о форматированиях, применяемых к подстанте текста фигуры, если раздел Символы содержит несколько строк.</span><span class="sxs-lookup"><span data-stu-id="71047-112">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows.</span></span> <span data-ttu-id="71047-113">В противном случае он содержит сведения о формате для всего текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="71047-113">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="71047-114">Вы также можете установить значение этой ячейки с помощью диалогового окна **Text** (щелкните стрелку **Шрифта** на вкладке **Главная).**</span><span class="sxs-lookup"><span data-stu-id="71047-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="71047-115">Чтобы получить ссылку на ячейку DoubleULine по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="71047-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71047-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="71047-116">Cell name:</span></span>  <br/> |<span data-ttu-id="71047-117">Char.DblUnderline[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="71047-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="71047-118">Чтобы получить ссылку на ячейку DoubleULine по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="71047-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71047-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="71047-119">Section index:</span></span>  <br/> |<span data-ttu-id="71047-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="71047-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="71047-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="71047-121">Row index:</span></span>  <br/> |<span data-ttu-id="71047-122">**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="71047-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="71047-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="71047-123">Cell index:</span></span>  <br/> |<span data-ttu-id="71047-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="71047-124">**visCharacterDblUnderline**</span></span> <br/> |
   

