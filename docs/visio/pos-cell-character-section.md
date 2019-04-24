---
title: Pos Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Определяет положение текста фигуры относительно базового плана.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359817"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="79bd6-103">Pos Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="79bd6-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="79bd6-104">Определяет положение текста фигуры относительно базового плана.</span><span class="sxs-lookup"><span data-stu-id="79bd6-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="79bd6-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="79bd6-105">**Value**</span></span>|<span data-ttu-id="79bd6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="79bd6-106">**Description**</span></span>|<span data-ttu-id="79bd6-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="79bd6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="79bd6-108">нуль</span><span class="sxs-lookup"><span data-stu-id="79bd6-108">0</span></span>  <br/> | <span data-ttu-id="79bd6-109">Обычное положение</span><span class="sxs-lookup"><span data-stu-id="79bd6-109">Normal position</span></span>  <br/> |<span data-ttu-id="79bd6-110">**Виспоснормал**</span><span class="sxs-lookup"><span data-stu-id="79bd6-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="79bd6-111">1,1</span><span class="sxs-lookup"><span data-stu-id="79bd6-111">1</span></span>  <br/> | <span data-ttu-id="79bd6-112">Superscript</span><span class="sxs-lookup"><span data-stu-id="79bd6-112">Superscript</span></span>  <br/> |<span data-ttu-id="79bd6-113">**Виспоссупер**</span><span class="sxs-lookup"><span data-stu-id="79bd6-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="79bd6-114">2</span><span class="sxs-lookup"><span data-stu-id="79bd6-114">2</span></span>  <br/> | <span data-ttu-id="79bd6-115">Subscript</span><span class="sxs-lookup"><span data-stu-id="79bd6-115">Subscript</span></span>  <br/> |<span data-ttu-id="79bd6-116">**Виспоссуб**</span><span class="sxs-lookup"><span data-stu-id="79bd6-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79bd6-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="79bd6-117">Remarks</span></span>

<span data-ttu-id="79bd6-118">Чтобы получить ссылку на ячейку POS по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="79bd6-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79bd6-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="79bd6-119">Cell name:</span></span>  <br/> | <span data-ttu-id="79bd6-120">Char. POS [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="79bd6-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="79bd6-121">Чтобы получить ссылку на ячейку POS по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="79bd6-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79bd6-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="79bd6-122">Section index:</span></span>  <br/> |<span data-ttu-id="79bd6-123">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="79bd6-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="79bd6-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="79bd6-124">Row index:</span></span>  <br/> |<span data-ttu-id="79bd6-125">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="79bd6-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="79bd6-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="79bd6-126">Cell index:</span></span>  <br/> |<span data-ttu-id="79bd6-127">**Висчарактерпос**</span><span class="sxs-lookup"><span data-stu-id="79bd6-127">**visCharacterPos**</span></span> <br/> |
   

