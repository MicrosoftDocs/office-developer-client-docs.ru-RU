---
title: Value Cell (User-Defined Cells Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Задает значение для соответствующей пользовательской ячейки.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422992"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="dfca7-103">Value Cell (User-Defined Cells Section)</span><span class="sxs-lookup"><span data-stu-id="dfca7-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="dfca7-104">Задает значение для соответствующей пользовательской ячейки.</span><span class="sxs-lookup"><span data-stu-id="dfca7-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfca7-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="dfca7-105">Remarks</span></span>

<span data-ttu-id="dfca7-106">Чтобы сослаться на это значение в другой ячейке, укажите пользовательское имя, введенное в поле Подпись строки User. Row.</span><span class="sxs-lookup"><span data-stu-id="dfca7-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="dfca7-107">Чтобы получить ссылку на ячейку значения по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="dfca7-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfca7-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dfca7-108">Cell name:</span></span>  <br/> | <span data-ttu-id="dfca7-109">Пользователем.</span><span class="sxs-lookup"><span data-stu-id="dfca7-109">User.</span></span>  <span data-ttu-id="dfca7-110">*Name (имя* ). Значение, где пользователь.</span><span class="sxs-lookup"><span data-stu-id="dfca7-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="dfca7-111">*Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="dfca7-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="dfca7-112">Чтобы получить ссылку на ячейку value по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dfca7-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfca7-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dfca7-113">Section index:</span></span>  <br/> |<span data-ttu-id="dfca7-114">**виссектионусер**</span><span class="sxs-lookup"><span data-stu-id="dfca7-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="dfca7-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dfca7-115">Row index:</span></span>  <br/> |<span data-ttu-id="dfca7-116">**висровусер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dfca7-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dfca7-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dfca7-117">Cell index:</span></span>  <br/> |<span data-ttu-id="dfca7-118">**висусервалуе**</span><span class="sxs-lookup"><span data-stu-id="dfca7-118">**visUserValue**</span></span> <br/> |
   

