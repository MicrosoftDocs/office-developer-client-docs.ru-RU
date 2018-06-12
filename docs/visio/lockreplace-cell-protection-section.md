---
title: Ячейка LockReplace (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Указывает, является ли фигура может принимать участие в операции замены (в качестве целевого или фигуры замещения).
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814138"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="c2a68-103">Ячейка LockReplace (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="c2a68-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="c2a68-104">Указывает, является ли фигура может принимать участие в операции замены (в качестве целевого или фигуры замещения).</span><span class="sxs-lookup"><span data-stu-id="c2a68-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="c2a68-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c2a68-105">**Value**</span></span>|<span data-ttu-id="c2a68-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c2a68-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2a68-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c2a68-107">TRUE</span></span>  <br/> |<span data-ttu-id="c2a68-108">Фигура не может быть заменен или использовать в качестве замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2a68-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="c2a68-109">Для фигуры на полотно кнопка **Изменить фигуру** отключена при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2a68-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="c2a68-110">Фигуры в наборе элементов фигуры не отображается как фигуры замещения, при нажатии кнопки **Изменить фигуру** .</span><span class="sxs-lookup"><span data-stu-id="c2a68-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="c2a68-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c2a68-111">FALSE</span></span>  <br/> |<span data-ttu-id="c2a68-112">Форму можно заменить или использовать в качестве замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2a68-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2a68-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2a68-113">Remarks</span></span>

<span data-ttu-id="c2a68-114">Для получения ссылки на ячейки **LockReplace** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="c2a68-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2a68-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c2a68-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c2a68-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="c2a68-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="c2a68-117">Для получения ссылки на ячейки **LockReplace** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c2a68-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2a68-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c2a68-118">Section index:</span></span>  <br/> |<span data-ttu-id="c2a68-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2a68-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c2a68-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c2a68-120">Row index:</span></span>  <br/> |<span data-ttu-id="c2a68-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c2a68-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c2a68-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2a68-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c2a68-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="c2a68-123">**visLockReplace**</span></span> <br/> |
   

