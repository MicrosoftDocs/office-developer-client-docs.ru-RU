---
title: D Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Ячейка нуля, которую можно использовать для ввода или тестирования формул.
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408175"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="b1899-103">D Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="b1899-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="b1899-104">Ячейка нуля, которую можно использовать для ввода или тестирования формул.</span><span class="sxs-lookup"><span data-stu-id="b1899-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1899-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1899-105">Remarks</span></span>

<span data-ttu-id="b1899-106">Чтобы получить доступ к ячейке D, щелкните правой кнопкой мыши строку и нажмите **кнопку Изменить** строку в меню ярлыка.</span><span class="sxs-lookup"><span data-stu-id="b1899-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="b1899-107">Чтобы получить ссылку на ячейку D по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b1899-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1899-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b1899-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b1899-109">Connections.D[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b1899-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b1899-110">Чтобы получить ссылку на ячейку D по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b1899-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1899-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b1899-111">Section index:</span></span>  <br/> |<span data-ttu-id="b1899-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="b1899-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="b1899-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b1899-113">Row index:</span></span>  <br/> |<span data-ttu-id="b1899-114">**visRowConnectionPts** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="b1899-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b1899-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b1899-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b1899-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="b1899-116">**visCnnctD**</span></span> <br/> |
   

