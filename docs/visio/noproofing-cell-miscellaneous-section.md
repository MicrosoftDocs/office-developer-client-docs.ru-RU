---
title: NoProofing Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Определяет, исправляются ли правописание автоматически и отображаются ли орфографические ошибки для выбранной фигуры. Принимает логическое значение.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431255"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="5c13b-104">NoProofing Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="5c13b-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5c13b-105">Определяет, исправляются ли правописание автоматически и отображаются ли орфографические ошибки для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="5c13b-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="5c13b-106">Принимает **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="5c13b-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="5c13b-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5c13b-107">**Value**</span></span>|<span data-ttu-id="5c13b-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c13b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c13b-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="5c13b-109">TRUE</span></span>  <br/> |<span data-ttu-id="5c13b-110">Проверка орфографии не выполняется автоматически, а орфографические ошибки не отображаются для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="5c13b-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="5c13b-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="5c13b-111">FALSE</span></span>  <br/> |<span data-ttu-id="5c13b-112">Проверка правописания автоматически исправляется и для выбранной фигуры отображаются орфографические ошибки.</span><span class="sxs-lookup"><span data-stu-id="5c13b-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c13b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c13b-113">Remarks</span></span>

<span data-ttu-id="5c13b-114">Чтобы получить ссылку на ячейку с параметром "Правописание" с помощью имени из другой формулы или из программы, используйте свойство **CellsU** :</span><span class="sxs-lookup"><span data-stu-id="5c13b-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c13b-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c13b-115">Cell name:</span></span>  <br/> |<span data-ttu-id="5c13b-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="5c13b-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="5c13b-117">Чтобы получить ссылку на ячейку "unproofing" по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5c13b-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c13b-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5c13b-118">Section index:</span></span>  <br/> |<span data-ttu-id="5c13b-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c13b-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5c13b-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5c13b-120">Row index:</span></span>  <br/> |<span data-ttu-id="5c13b-121">**висровмиск**</span><span class="sxs-lookup"><span data-stu-id="5c13b-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="5c13b-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c13b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5c13b-123">**висобжнопруфинг**</span><span class="sxs-lookup"><span data-stu-id="5c13b-123">**visObjNoProofing**</span></span> <br/> |
   

