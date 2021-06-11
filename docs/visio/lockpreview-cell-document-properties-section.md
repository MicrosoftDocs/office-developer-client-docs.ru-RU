---
title: LockPreview Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Определяет, сохраняется ли предварительный просмотр при каждом сохранения рисунка.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418864"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="2b239-103">LockPreview Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="2b239-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="2b239-104">Определяет, сохраняется ли предварительный просмотр при каждом сохранения рисунка.</span><span class="sxs-lookup"><span data-stu-id="2b239-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="2b239-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2b239-105">**Value**</span></span>|<span data-ttu-id="2b239-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b239-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2b239-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2b239-107">TRUE</span></span>  <br/> | <span data-ttu-id="2b239-108">Не экономите предварительный просмотр при каждом сохранения рисунка.</span><span class="sxs-lookup"><span data-stu-id="2b239-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="2b239-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2b239-109">FALSE</span></span>  <br/> | <span data-ttu-id="2b239-110">Сохраните предварительный просмотр при каждом сохранения рисунка.</span><span class="sxs-lookup"><span data-stu-id="2b239-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b239-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b239-111">Remarks</span></span>

<span data-ttu-id="2b239-112">Чтобы получить ссылку на ячейку LockPreview по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="2b239-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b239-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2b239-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2b239-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="2b239-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="2b239-115">Чтобы получить ссылку на ячейку LockPreview по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2b239-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b239-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2b239-116">Section index:</span></span>  <br/> |<span data-ttu-id="2b239-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2b239-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2b239-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2b239-118">Row index:</span></span>  <br/> |<span data-ttu-id="2b239-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="2b239-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="2b239-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2b239-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2b239-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="2b239-121">**visDocLockPreview**</span></span> <br/> |
   

