---
title: Ячейка RotateGradientWithShape (градиента Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Определяет, разворачивает ли градиентной заливки с фигуры в 2D вращение типа Boolean.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814619"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="be563-103">Ячейка RotateGradientWithShape (градиента Properties Section)</span><span class="sxs-lookup"><span data-stu-id="be563-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="be563-104">Определяет, разворачивает ли градиентной заливки с фигуры в 2D вращение типа Boolean.</span><span class="sxs-lookup"><span data-stu-id="be563-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="be563-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="be563-105">**Value**</span></span>|<span data-ttu-id="be563-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be563-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be563-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="be563-107">TRUE</span></span>  <br/> |<span data-ttu-id="be563-108">Градиента поворот с фигурой при фигуры является вращаться вокруг вращение ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="be563-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="be563-109">«Начало» градиента параллельного маркер вращения.</span><span class="sxs-lookup"><span data-stu-id="be563-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="be563-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="be563-110">FALSE</span></span>  <br/> |<span data-ttu-id="be563-111">Градиент не Поворачивайте с фигурой при фигуры является вращаться вокруг вращение ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="be563-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="be563-112">«Начало» градиента параллельного полотно.</span><span class="sxs-lookup"><span data-stu-id="be563-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be563-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="be563-113">Remarks</span></span>

<span data-ttu-id="be563-114">Для получения ссылки на ячейки **RotateGradientWithShape** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="be563-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be563-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="be563-115">Cell name:</span></span>  <br/> | <span data-ttu-id="be563-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="be563-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="be563-117">Для получения ссылки на ячейки **RotateGradientWithShape** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="be563-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be563-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="be563-118">Section index:</span></span>  <br/> |<span data-ttu-id="be563-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="be563-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="be563-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="be563-120">Row index:</span></span>  <br/> |<span data-ttu-id="be563-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="be563-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="be563-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="be563-122">Cell index:</span></span>  <br/> |<span data-ttu-id="be563-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="be563-123">**visRotateGradientWithShape**</span></span> <br/> |
   

