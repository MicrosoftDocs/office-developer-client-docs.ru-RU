---
title: Ячейка Value (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Содержит значение элемента данных фигуры, введенное в диалоговом окне "Определение данных фигуры".
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815136"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="bc04f-103">Ячейка Value (раздел "Данные фигуры")</span><span class="sxs-lookup"><span data-stu-id="bc04f-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="bc04f-104">Содержит значение элемента данных фигуры, введенное в диалоговом окне " **Определение данных фигуры** ".</span><span class="sxs-lookup"><span data-stu-id="bc04f-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc04f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc04f-105">Remarks</span></span>

<span data-ttu-id="bc04f-106">Содержащиеся в этой ячейке формулы заменяются на значения, введенные в диалоговом окне **Определение данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="bc04f-106">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="bc04f-107">Это значение true, даже в том случае, если функция защиты для защиты формулу.</span><span class="sxs-lookup"><span data-stu-id="bc04f-107">This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="bc04f-108">Чтобы получить ссылку на значение ячейки по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="bc04f-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc04f-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bc04f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="bc04f-110">Свойства.  *Имя* . Значение где свойств.  *Имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="bc04f-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="bc04f-111">Для получения ссылки на ячейки значение по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bc04f-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc04f-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bc04f-112">Section index:</span></span>  <br/> |<span data-ttu-id="bc04f-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="bc04f-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="bc04f-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bc04f-114">Row index:</span></span>  <br/> |<span data-ttu-id="bc04f-115">**visRowProp** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bc04f-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bc04f-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bc04f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bc04f-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="bc04f-117">**visCustPropsValue**</span></span> <br/> |
   

