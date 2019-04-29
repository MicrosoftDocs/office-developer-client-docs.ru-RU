---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Указывает, будет ли текст фигуры игнорировать Поворот фигуры в трехмерном виде. Не применяется к повороту на 2 D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422042"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="4f258-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span><span class="sxs-lookup"><span data-stu-id="4f258-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="4f258-105">Указывает, будет ли текст фигуры игнорировать Поворот фигуры в трехмерном виде.</span><span class="sxs-lookup"><span data-stu-id="4f258-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="4f258-106">Не применяется к повороту на 2 D.</span><span class="sxs-lookup"><span data-stu-id="4f258-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="4f258-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4f258-107">**Value**</span></span>|<span data-ttu-id="4f258-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f258-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f258-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="4f258-109">TRUE</span></span>  <br/> |<span data-ttu-id="4f258-110">Текст фигуры не поворачивается вместе с геометрическим объектом фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f258-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="4f258-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="4f258-111">FALSE</span></span>  <br/> |<span data-ttu-id="4f258-112">Текст фигуры преобразуется в поворот с помощью геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f258-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f258-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f258-113">Remarks</span></span>

<span data-ttu-id="4f258-114">Чтобы получить ссылку на ячейку **KeepTextFlat** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="4f258-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f258-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4f258-115">Cell name:</span></span>  <br/> |<span data-ttu-id="4f258-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="4f258-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="4f258-117">Чтобы получить ссылку на ячейку **KeepTextFlat** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4f258-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f258-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4f258-118">Section index:</span></span>  <br/> |<span data-ttu-id="4f258-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4f258-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4f258-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4f258-120">Row index:</span></span>  <br/> |<span data-ttu-id="4f258-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="4f258-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="4f258-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4f258-122">Cell index:</span></span>  <br/> |<span data-ttu-id="4f258-123">**Вискиптекстфлат**</span><span class="sxs-lookup"><span data-stu-id="4f258-123">**visKeepTextFlat**</span></span> <br/> |
   

