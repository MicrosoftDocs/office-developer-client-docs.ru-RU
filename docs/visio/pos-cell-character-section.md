---
title: Ячейка Pos (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Определяет положение текста фигуры относительно базового плана.
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814468"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="7234e-103">Ячейка Pos (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="7234e-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="7234e-104">Определяет положение текста фигуры относительно базового плана.</span><span class="sxs-lookup"><span data-stu-id="7234e-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="7234e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7234e-105">**Value**</span></span>|<span data-ttu-id="7234e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7234e-106">**Description**</span></span>|<span data-ttu-id="7234e-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="7234e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7234e-108">0</span><span class="sxs-lookup"><span data-stu-id="7234e-108">0</span></span>  <br/> | <span data-ttu-id="7234e-109">Обычном положении</span><span class="sxs-lookup"><span data-stu-id="7234e-109">Normal position</span></span>  <br/> |<span data-ttu-id="7234e-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="7234e-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="7234e-111">1</span><span class="sxs-lookup"><span data-stu-id="7234e-111">1</span></span>  <br/> | <span data-ttu-id="7234e-112">Надстрочный знак</span><span class="sxs-lookup"><span data-stu-id="7234e-112">Superscript</span></span>  <br/> |<span data-ttu-id="7234e-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="7234e-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="7234e-114">2</span><span class="sxs-lookup"><span data-stu-id="7234e-114">2</span></span>  <br/> | <span data-ttu-id="7234e-115">Подстрочный знак</span><span class="sxs-lookup"><span data-stu-id="7234e-115">Subscript</span></span>  <br/> |<span data-ttu-id="7234e-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="7234e-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7234e-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="7234e-117">Remarks</span></span>

<span data-ttu-id="7234e-118">Чтобы получить ссылку на ячейку положительные по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7234e-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7234e-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="7234e-119">Cell name:</span></span>  <br/> | <span data-ttu-id="7234e-120">Char.Pos [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7234e-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7234e-121">Для получения ссылки на ячейки положительные по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="7234e-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7234e-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7234e-122">Section index:</span></span>  <br/> |<span data-ttu-id="7234e-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7234e-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="7234e-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7234e-124">Row index:</span></span>  <br/> |<span data-ttu-id="7234e-125">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7234e-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7234e-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7234e-126">Cell index:</span></span>  <br/> |<span data-ttu-id="7234e-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="7234e-127">**visCharacterPos**</span></span> <br/> |
   

