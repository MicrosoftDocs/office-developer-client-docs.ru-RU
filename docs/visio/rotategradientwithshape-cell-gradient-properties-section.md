---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Определяет, вращается ли Градиентная заливка с фигурой в двухмерном повороте в виде логического значения.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315661"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="04bf5-103">RotateGradientWithShape Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="04bf5-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="04bf5-104">Определяет, вращается ли Градиентная заливка с фигурой в двухмерном повороте в виде логического значения.</span><span class="sxs-lookup"><span data-stu-id="04bf5-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="04bf5-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="04bf5-105">**Value**</span></span>|<span data-ttu-id="04bf5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04bf5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04bf5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="04bf5-107">TRUE</span></span>  <br/> |<span data-ttu-id="04bf5-108">Градиент поворачивается вместе с фигурой, когда фигура поворачивается вокруг ПИН-кода вращения.</span><span class="sxs-lookup"><span data-stu-id="04bf5-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="04bf5-109">"Top" градиента параллельно с маркером вращения.</span><span class="sxs-lookup"><span data-stu-id="04bf5-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="04bf5-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="04bf5-110">FALSE</span></span>  <br/> |<span data-ttu-id="04bf5-111">Градиент не поворачивается вместе с фигурой, когда фигура вращается вокруг ПИН-кода вращения.</span><span class="sxs-lookup"><span data-stu-id="04bf5-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="04bf5-112">"Top" градиента параллельно с полотном.</span><span class="sxs-lookup"><span data-stu-id="04bf5-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04bf5-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="04bf5-113">Remarks</span></span>

<span data-ttu-id="04bf5-114">Чтобы получить ссылку на ячейку **RotateGradientWithShape** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="04bf5-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04bf5-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="04bf5-115">Cell name:</span></span>  <br/> | <span data-ttu-id="04bf5-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="04bf5-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="04bf5-117">Чтобы получить ссылку на ячейку **RotateGradientWithShape** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="04bf5-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04bf5-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="04bf5-118">Section index:</span></span>  <br/> |<span data-ttu-id="04bf5-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="04bf5-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="04bf5-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="04bf5-120">Row index:</span></span>  <br/> |<span data-ttu-id="04bf5-121">**Висровградиентпропертиес**</span><span class="sxs-lookup"><span data-stu-id="04bf5-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="04bf5-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="04bf5-122">Cell index:</span></span>  <br/> |<span data-ttu-id="04bf5-123">**Висротатеградиентвисшапе**</span><span class="sxs-lookup"><span data-stu-id="04bf5-123">**visRotateGradientWithShape**</span></span> <br/> |
   

