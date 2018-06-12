---
title: Ячейка LockCalcWH (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Блокирует прямоугольник выделения фигуры, чтобы ее нельзя было обновить при редактировании узел или изменить тип строки в раздел геометрии.
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814119"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="127cb-103">Ячейка LockCalcWH (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="127cb-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="127cb-104">Блокирует прямоугольник выделения фигуры, чтобы ее нельзя было обновить при редактировании узел или изменить тип строки в раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="127cb-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="127cb-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="127cb-105">**Value**</span></span>|<span data-ttu-id="127cb-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="127cb-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="127cb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="127cb-107">TRUE</span></span>  <br/> | <span data-ttu-id="127cb-108">Не удалось обновить ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="127cb-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="127cb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="127cb-109">FALSE</span></span>  <br/> | <span data-ttu-id="127cb-110">Можно перерасчете ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="127cb-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="127cb-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="127cb-111">Remarks</span></span>

<span data-ttu-id="127cb-112">Чтобы получить ссылку на ячейку LockCalcWH по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="127cb-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="127cb-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="127cb-113">Cell name:</span></span>  <br/> | <span data-ttu-id="127cb-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="127cb-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="127cb-115">Для получения ссылки на ячейки LockCalcWH по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="127cb-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="127cb-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="127cb-116">Section index:</span></span>  <br/> |<span data-ttu-id="127cb-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="127cb-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="127cb-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="127cb-118">Row index:</span></span>  <br/> |<span data-ttu-id="127cb-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="127cb-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="127cb-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="127cb-120">Cell index:</span></span>  <br/> |<span data-ttu-id="127cb-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="127cb-121">**visLockCalcWH**</span></span> <br/> |
   

