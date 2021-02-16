---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Определяет, будет ли орфографическая ошибка автоматически исправлена и отображаются ли ошибки орфографии для выбранной фигуры. Принимает значение boolean.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431255"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="316d7-104">NoProofing Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="316d7-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="316d7-105">Определяет, будет ли орфографическая ошибка автоматически исправлена и отображаются ли ошибки орфографии для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="316d7-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="316d7-106">Принимает значение **boolean.**</span><span class="sxs-lookup"><span data-stu-id="316d7-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="316d7-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="316d7-107">**Value**</span></span>|<span data-ttu-id="316d7-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="316d7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="316d7-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="316d7-109">TRUE</span></span>  <br/> |<span data-ttu-id="316d7-110">Орфография не исправлена автоматически, а для выбранной фигуры не отображаются ошибки орфографии.</span><span class="sxs-lookup"><span data-stu-id="316d7-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="316d7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="316d7-111">FALSE</span></span>  <br/> |<span data-ttu-id="316d7-112">Орфография автоматически исправляется, и для выбранной фигуры отображаются ошибки орфографии.</span><span class="sxs-lookup"><span data-stu-id="316d7-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="316d7-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="316d7-113">Remarks</span></span>

<span data-ttu-id="316d7-114">Чтобы получить ссылку на ячейку NoProofing по имени из другой формулы или из программы, используя свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="316d7-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="316d7-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="316d7-115">Cell name:</span></span>  <br/> |<span data-ttu-id="316d7-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="316d7-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="316d7-117">Чтобы получить ссылку на ячейку NoProofing по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="316d7-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="316d7-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="316d7-118">Section index:</span></span>  <br/> |<span data-ttu-id="316d7-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="316d7-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="316d7-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="316d7-120">Row index:</span></span>  <br/> |<span data-ttu-id="316d7-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="316d7-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="316d7-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="316d7-122">Cell index:</span></span>  <br/> |<span data-ttu-id="316d7-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="316d7-123">**visObjNoProofing**</span></span> <br/> |
   

