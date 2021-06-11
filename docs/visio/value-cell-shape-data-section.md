---
title: Value Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Содержит значение элемента данных фигуры, вступив в диалоговое окно Define Shape Data.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431906"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="92948-103">Value Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="92948-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="92948-104">Содержит значение элемента данных фигуры, вступив в диалоговое окно **Define Shape Data.**</span><span class="sxs-lookup"><span data-stu-id="92948-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="92948-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="92948-105">Remarks</span></span>

<span data-ttu-id="92948-106">Формулы, вступив в эту ячейку, переопределяются значениями, вписав их в диалоговое окно **Define Shape Data.**</span><span class="sxs-lookup"><span data-stu-id="92948-106">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="92948-107">Это верно, даже если для защиты формулы используется функция GUARD.</span><span class="sxs-lookup"><span data-stu-id="92948-107">This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="92948-108">Чтобы получить ссылку на ячейку Value по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="92948-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="92948-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="92948-109">Cell name:</span></span>  <br/> | <span data-ttu-id="92948-110">Prop.  *Имя*  . Значение, в котором prop.  *Имя*  — это имя строки</span><span class="sxs-lookup"><span data-stu-id="92948-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="92948-111">Чтобы получить ссылку на ячейку Value по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="92948-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="92948-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="92948-112">Section index:</span></span>  <br/> |<span data-ttu-id="92948-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="92948-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="92948-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="92948-114">Row index:</span></span>  <br/> |<span data-ttu-id="92948-115">**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="92948-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="92948-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="92948-116">Cell index:</span></span>  <br/> |<span data-ttu-id="92948-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="92948-117">**visCustPropsValue**</span></span> <br/> |
   

