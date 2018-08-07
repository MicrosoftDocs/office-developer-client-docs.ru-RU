---
title: Ячейка Can Glue (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Определяет, может ли быть связан дескриптор элемента управления на другие фигуры.
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813307"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="dec65-103">Ячейка Can Glue (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="dec65-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="dec65-104">Определяет, может ли быть связан дескриптор элемента управления на другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="dec65-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="dec65-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="dec65-105">**Value**</span></span>|<span data-ttu-id="dec65-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dec65-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dec65-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dec65-107">TRUE</span></span>  <br/> | <span data-ttu-id="dec65-108">Может быть связан дескриптора элемента управления.</span><span class="sxs-lookup"><span data-stu-id="dec65-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="dec65-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dec65-109">FALSE</span></span>  <br/> | <span data-ttu-id="dec65-110">Не может быть связан дескриптора элемента управления.</span><span class="sxs-lookup"><span data-stu-id="dec65-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dec65-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="dec65-111">Remarks</span></span>

<span data-ttu-id="dec65-112">Чтобы получить ссылку на ячейку можно связывающих по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dec65-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dec65-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="dec65-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dec65-114">Элементы управления.</span><span class="sxs-lookup"><span data-stu-id="dec65-114">Controls.</span></span>  <span data-ttu-id="dec65-115">*имя* . Элементы управления CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="dec65-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="dec65-116">*имя* — это имя строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="dec65-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="dec65-117">Для получения ссылки на ячейки можно связывающих по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="dec65-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dec65-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dec65-118">Section index:</span></span>  <br/> |<span data-ttu-id="dec65-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="dec65-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="dec65-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dec65-120">Row index:</span></span>  <br/> |<span data-ttu-id="dec65-121">**visRowControl** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="dec65-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="dec65-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dec65-122">Cell index:</span></span>  <br/> |<span data-ttu-id="dec65-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="dec65-123">**visCtlGlue**</span></span> <br/> |
   

