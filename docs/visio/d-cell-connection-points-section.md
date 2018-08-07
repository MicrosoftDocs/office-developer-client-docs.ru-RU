---
title: Ячейка D (раздел "Точки соединения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Вспомогательной ячеек, которые можно использовать для ввода и проверки формул.
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813527"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="b559b-103">Ячейка D (раздел "Точки соединения")</span><span class="sxs-lookup"><span data-stu-id="b559b-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="b559b-104">Вспомогательной ячеек, которые можно использовать для ввода и проверки формул.</span><span class="sxs-lookup"><span data-stu-id="b559b-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b559b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b559b-105">Remarks</span></span>

<span data-ttu-id="b559b-106">Для доступа к ячейке D, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="b559b-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="b559b-107">Чтобы получить ссылку на ячейке D по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b559b-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b559b-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b559b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b559b-109">Connections.D [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b559b-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b559b-110">Для получения ссылки на ячейки D по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b559b-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b559b-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b559b-111">Section index:</span></span>  <br/> |<span data-ttu-id="b559b-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="b559b-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="b559b-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b559b-113">Row index:</span></span>  <br/> |<span data-ttu-id="b559b-114">**visRowConnectionPts** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b559b-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b559b-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b559b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b559b-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="b559b-116">**visCnnctD**</span></span> <br/> |
   

