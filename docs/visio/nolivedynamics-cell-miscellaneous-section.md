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
description: Определяет, будет ли фигура динамически изменять размер или поворачиваться при управлении ею.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340987"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="c596c-103">NoLiveDynamics Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="c596c-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c596c-104">Определяет, будет ли фигура динамически изменять размер или поворачиваться при управлении ею.</span><span class="sxs-lookup"><span data-stu-id="c596c-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="c596c-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="c596c-105">**Value**</span></span>|<span data-ttu-id="c596c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c596c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c596c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c596c-107">TRUE</span></span>  <br/> | <span data-ttu-id="c596c-108">Не обновляйте фигуру динамически при управлении ею.</span><span class="sxs-lookup"><span data-stu-id="c596c-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="c596c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c596c-109">FALSE</span></span>  <br/> | <span data-ttu-id="c596c-110">Динамическое обновление фигуры во время управления ею.</span><span class="sxs-lookup"><span data-stu-id="c596c-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c596c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c596c-111">Remarks</span></span>

<span data-ttu-id="c596c-112">При изменении размера или повороте двухмерной (2-D) фигуры без динамического Dynamics отображается поле выбора.</span><span class="sxs-lookup"><span data-stu-id="c596c-112">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box.</span></span> <span data-ttu-id="c596c-113">Если фигура является одномерным (1-D), визуальная обратная связь основывается на значении в ячейке DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="c596c-113">If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="c596c-114">Чтобы получить ссылку на ячейку NoLiveDynamics по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c596c-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c596c-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c596c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c596c-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="c596c-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="c596c-117">Чтобы получить ссылку на ячейку NoLiveDynamics по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c596c-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c596c-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c596c-118">Section index:</span></span>  <br/> |<span data-ttu-id="c596c-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c596c-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c596c-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c596c-120">Row index:</span></span>  <br/> |<span data-ttu-id="c596c-121">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="c596c-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c596c-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c596c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c596c-123">**Висноливединамикс**</span><span class="sxs-lookup"><span data-stu-id="c596c-123">**visNoLiveDynamics**</span></span> <br/> |
   

