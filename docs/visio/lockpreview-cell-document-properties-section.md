---
title: Ячейка LockPreview (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Определяет, сохраняется ли Предварительный просмотр каждый раз при сохранении документа.
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814142"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="f7db9-103">Ячейка LockPreview (раздел "Свойства документа")</span><span class="sxs-lookup"><span data-stu-id="f7db9-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="f7db9-104">Определяет, сохраняется ли Предварительный просмотр каждый раз при сохранении документа.</span><span class="sxs-lookup"><span data-stu-id="f7db9-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="f7db9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f7db9-105">**Value**</span></span>|<span data-ttu-id="f7db9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f7db9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f7db9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f7db9-107">TRUE</span></span>  <br/> | <span data-ttu-id="f7db9-108">Не следует сохранять предварительной версии каждый раз, когда сохранения документа.</span><span class="sxs-lookup"><span data-stu-id="f7db9-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="f7db9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f7db9-109">FALSE</span></span>  <br/> | <span data-ttu-id="f7db9-110">Сохраните предварительной версии каждый раз, когда сохранения документа.</span><span class="sxs-lookup"><span data-stu-id="f7db9-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7db9-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7db9-111">Remarks</span></span>

<span data-ttu-id="f7db9-112">Чтобы получить ссылку на ячейку LockPreview по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f7db9-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7db9-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="f7db9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f7db9-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="f7db9-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="f7db9-115">Для получения ссылки на ячейки LockPreview по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="f7db9-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7db9-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f7db9-116">Section index:</span></span>  <br/> |<span data-ttu-id="f7db9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f7db9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f7db9-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f7db9-118">Row index:</span></span>  <br/> |<span data-ttu-id="f7db9-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="f7db9-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="f7db9-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f7db9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f7db9-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="f7db9-121">**visDocLockPreview**</span></span> <br/> |
   

