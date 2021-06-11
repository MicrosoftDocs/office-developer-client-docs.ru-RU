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
description: Определяет, меняется ли фигура динамически или вращается при ее манипулировании.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421482"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="69485-103">NoLiveDynamics Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="69485-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="69485-104">Определяет, меняется ли фигура динамически или вращается при ее манипулировании.</span><span class="sxs-lookup"><span data-stu-id="69485-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="69485-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="69485-105">**Value**</span></span>|<span data-ttu-id="69485-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="69485-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="69485-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="69485-107">TRUE</span></span>  <br/> | <span data-ttu-id="69485-108">Не обновляй фигуру динамически во время ее обработки.</span><span class="sxs-lookup"><span data-stu-id="69485-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="69485-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="69485-109">FALSE</span></span>  <br/> | <span data-ttu-id="69485-110">Динамически обновив форму во время ее обработки.</span><span class="sxs-lookup"><span data-stu-id="69485-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69485-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="69485-111">Remarks</span></span>

<span data-ttu-id="69485-112">При повторном размере или повороте двухмерной (2-D) формы без живой динамики вы увидите поле выбора.</span><span class="sxs-lookup"><span data-stu-id="69485-112">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box.</span></span> <span data-ttu-id="69485-113">Если форма одномерная (1-D), визуальная обратная связь основана на значении ячейки DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="69485-113">If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="69485-114">Чтобы получить ссылку на ячейку NoLiveDynamics по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="69485-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69485-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="69485-115">Cell name:</span></span>  <br/> | <span data-ttu-id="69485-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="69485-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="69485-117">Чтобы получить ссылку на ячейку NoLiveDynamics по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="69485-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69485-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="69485-118">Section index:</span></span>  <br/> |<span data-ttu-id="69485-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="69485-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="69485-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="69485-120">Row index:</span></span>  <br/> |<span data-ttu-id="69485-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="69485-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="69485-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="69485-122">Cell index:</span></span>  <br/> |<span data-ttu-id="69485-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="69485-123">**visNoLiveDynamics**</span></span> <br/> |
   

