---
title: Ячейка Value (раздел "Пользовательские ячейки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Задает значение для соответствующей пользовательской ячейки.
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815131"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="45995-103">Ячейка Value (раздел "Пользовательские ячейки")</span><span class="sxs-lookup"><span data-stu-id="45995-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="45995-104">Задает значение для соответствующей пользовательской ячейки.</span><span class="sxs-lookup"><span data-stu-id="45995-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45995-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="45995-105">Remarks</span></span>

<span data-ttu-id="45995-106">Чтобы указать это значение в ячейке, укажите пользовательских имя, введенное в строке метки User.Row.</span><span class="sxs-lookup"><span data-stu-id="45995-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="45995-107">Чтобы получить ссылку на значение ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="45995-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45995-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="45995-108">Cell name:</span></span>  <br/> | <span data-ttu-id="45995-109">Пользователь.</span><span class="sxs-lookup"><span data-stu-id="45995-109">User.</span></span>  <span data-ttu-id="45995-110">*Имя* . Значение where пользователя.</span><span class="sxs-lookup"><span data-stu-id="45995-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="45995-111">*Имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="45995-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="45995-112">Для получения ссылки на ячейки значение по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="45995-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45995-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="45995-113">Section index:</span></span>  <br/> |<span data-ttu-id="45995-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="45995-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="45995-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="45995-115">Row index:</span></span>  <br/> |<span data-ttu-id="45995-116">**visRowUser** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="45995-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="45995-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="45995-117">Cell index:</span></span>  <br/> |<span data-ttu-id="45995-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="45995-118">**visUserValue**</span></span> <br/> |
   

