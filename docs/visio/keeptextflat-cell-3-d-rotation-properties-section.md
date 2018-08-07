---
title: Ячейка KeepTextFlat (раздел "Свойства поворота объемной фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Указывает, будет ли текстом фигуры будет игнорировать Поворот фигуры в объемных. Не применяется к плоских вращение.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814021"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="70c66-104">Ячейка KeepTextFlat (раздел "Свойства поворота объемной фигуры")</span><span class="sxs-lookup"><span data-stu-id="70c66-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="70c66-105">Указывает, будет ли текстом фигуры будет игнорировать Поворот фигуры в объемных.</span><span class="sxs-lookup"><span data-stu-id="70c66-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="70c66-106">Не применяется к плоских вращение.</span><span class="sxs-lookup"><span data-stu-id="70c66-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="70c66-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="70c66-107">**Value**</span></span>|<span data-ttu-id="70c66-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="70c66-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70c66-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="70c66-109">TRUE</span></span>  <br/> |<span data-ttu-id="70c66-110">Не поворачивайте текст фигуры с геометрией фигуры.</span><span class="sxs-lookup"><span data-stu-id="70c66-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="70c66-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="70c66-111">FALSE</span></span>  <br/> |<span data-ttu-id="70c66-112">Фигура текст преобразован в поворот с геометрией фигуры.</span><span class="sxs-lookup"><span data-stu-id="70c66-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70c66-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="70c66-113">Remarks</span></span>

<span data-ttu-id="70c66-114">Для получения ссылки на ячейки **KeepTextFlat** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="70c66-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70c66-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="70c66-115">Cell name:</span></span>  <br/> |<span data-ttu-id="70c66-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="70c66-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="70c66-117">Для получения ссылки на ячейки **KeepTextFlat** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="70c66-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70c66-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="70c66-118">Section index:</span></span>  <br/> |<span data-ttu-id="70c66-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="70c66-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="70c66-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="70c66-120">Row index:</span></span>  <br/> |<span data-ttu-id="70c66-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="70c66-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="70c66-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="70c66-122">Cell index:</span></span>  <br/> |<span data-ttu-id="70c66-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="70c66-123">**visKeepTextFlat**</span></span> <br/> |
   

