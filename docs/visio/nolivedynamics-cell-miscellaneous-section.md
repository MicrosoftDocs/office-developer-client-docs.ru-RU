---
title: NoLiveDynamics Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Определяет, динамически ли размер фигуры меняется или поворачивается при ее обработке.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421482"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="9cd5a-103">NoLiveDynamics Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="9cd5a-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="9cd5a-104">Определяет, динамически ли размер фигуры меняется или поворачивается при ее обработке.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="9cd5a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9cd5a-105">**Value**</span></span>|<span data-ttu-id="9cd5a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9cd5a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9cd5a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9cd5a-107">TRUE</span></span>  <br/> | <span data-ttu-id="9cd5a-108">Не обновляя фигуру динамически во время ее обработки.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="9cd5a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9cd5a-109">FALSE</span></span>  <br/> | <span data-ttu-id="9cd5a-110">Динамическое обновление фигуры во время ее обработки.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cd5a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="9cd5a-111">Remarks</span></span>

<span data-ttu-id="9cd5a-112">При вращающейся двумерной (двухмерной) фигуре без динамической динамики вы увидите поле выбора.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-112">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box.</span></span> <span data-ttu-id="9cd5a-113">Если фигура одномерная (одномерная), визуальная обратная связь зависит от значения ячейки DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-113">If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="9cd5a-114">Чтобы получить ссылку на ячейку NoLiveDynamics по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="9cd5a-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cd5a-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9cd5a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="9cd5a-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="9cd5a-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="9cd5a-117">Чтобы получить ссылку на ячейку NoLiveDynamics по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9cd5a-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cd5a-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9cd5a-118">Section index:</span></span>  <br/> |<span data-ttu-id="9cd5a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9cd5a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9cd5a-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9cd5a-120">Row index:</span></span>  <br/> |<span data-ttu-id="9cd5a-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="9cd5a-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="9cd5a-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9cd5a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="9cd5a-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="9cd5a-123">**visNoLiveDynamics**</span></span> <br/> |
   

