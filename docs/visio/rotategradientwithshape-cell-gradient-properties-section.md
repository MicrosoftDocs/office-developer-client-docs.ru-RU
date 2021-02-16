---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Определяет, вращается ли градиент заливки фигурой в 2D-повороте в виде boolean.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412221"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="ff0c0-103">RotateGradientWithShape Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ff0c0-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="ff0c0-104">Определяет, вращается ли градиент заливки фигурой в 2D-повороте в виде boolean.</span><span class="sxs-lookup"><span data-stu-id="ff0c0-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="ff0c0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ff0c0-105">**Value**</span></span>|<span data-ttu-id="ff0c0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ff0c0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff0c0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff0c0-107">TRUE</span></span>  <br/> |<span data-ttu-id="ff0c0-108">Градиент поворачивается вместе с фигурой при повороте фигуры вокруг закрепления поворота.</span><span class="sxs-lookup"><span data-stu-id="ff0c0-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="ff0c0-109">"Верхняя" часть градиента является параллельной вращаемой ладе.</span><span class="sxs-lookup"><span data-stu-id="ff0c0-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="ff0c0-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="ff0c0-110">FALSE</span></span>  <br/> |<span data-ttu-id="ff0c0-111">Градиент не поворачивается вместе с фигурой при повороте фигуры вокруг закрепления поворота.</span><span class="sxs-lookup"><span data-stu-id="ff0c0-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="ff0c0-112">"Верхняя" часть градиента является параллельно полотну.</span><span class="sxs-lookup"><span data-stu-id="ff0c0-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff0c0-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff0c0-113">Remarks</span></span>

<span data-ttu-id="ff0c0-114">Чтобы получить ссылку на ячейку **RotateGradientWithShape** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ff0c0-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff0c0-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ff0c0-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ff0c0-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="ff0c0-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="ff0c0-117">Чтобы получить ссылку на ячейку **RotateGradientWithShape** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ff0c0-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff0c0-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ff0c0-118">Section index:</span></span>  <br/> |<span data-ttu-id="ff0c0-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff0c0-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ff0c0-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ff0c0-120">Row index:</span></span>  <br/> |<span data-ttu-id="ff0c0-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="ff0c0-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="ff0c0-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ff0c0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ff0c0-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="ff0c0-123">**visRotateGradientWithShape**</span></span> <br/> |
   

