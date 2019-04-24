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
description: Определяет, сохраняется ли предварительный просмотр при каждом сохранении документа.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348330"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="0ea75-103">LockPreview Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="0ea75-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="0ea75-104">Определяет, сохраняется ли предварительный просмотр при каждом сохранении документа.</span><span class="sxs-lookup"><span data-stu-id="0ea75-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="0ea75-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="0ea75-105">**Value**</span></span>|<span data-ttu-id="0ea75-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0ea75-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0ea75-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0ea75-107">TRUE</span></span>  <br/> | <span data-ttu-id="0ea75-108">Не сохраняйте предварительный просмотр при каждом сохранении документа.</span><span class="sxs-lookup"><span data-stu-id="0ea75-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="0ea75-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0ea75-109">FALSE</span></span>  <br/> | <span data-ttu-id="0ea75-110">Сохраните предварительный просмотр при каждом сохранении документа.</span><span class="sxs-lookup"><span data-stu-id="0ea75-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ea75-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ea75-111">Remarks</span></span>

<span data-ttu-id="0ea75-112">Чтобы получить ссылку на ячейку LockPreview по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="0ea75-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ea75-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0ea75-113">Cell name:</span></span>  <br/> | <span data-ttu-id="0ea75-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="0ea75-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="0ea75-115">Чтобы получить ссылку на ячейку LockPreview по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0ea75-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ea75-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0ea75-116">Section index:</span></span>  <br/> |<span data-ttu-id="0ea75-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0ea75-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0ea75-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0ea75-118">Row index:</span></span>  <br/> |<span data-ttu-id="0ea75-119">**Висровдок**</span><span class="sxs-lookup"><span data-stu-id="0ea75-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="0ea75-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0ea75-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0ea75-121">**Висдоклоккпревиев**</span><span class="sxs-lookup"><span data-stu-id="0ea75-121">**visDocLockPreview**</span></span> <br/> |
   

