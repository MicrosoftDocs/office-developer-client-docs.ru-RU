---
title: Ячейка LockCrop (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Блокирует объект из другой программы от обрезки с помощью Обрезка.
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814125"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="ad495-103">Ячейка LockCrop (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="ad495-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="ad495-104">Блокирует объект из другой программы от обрезки с помощью **Обрезка** .</span><span class="sxs-lookup"><span data-stu-id="ad495-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="ad495-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ad495-105">**Value**</span></span>|<span data-ttu-id="ad495-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad495-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ad495-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ad495-107">TRUE</span></span>  <br/> | <span data-ttu-id="ad495-108">Не удается обрезки фигуры</span><span class="sxs-lookup"><span data-stu-id="ad495-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="ad495-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ad495-109">FALSE</span></span>  <br/> | <span data-ttu-id="ad495-110">Фигура может быть обрезки.</span><span class="sxs-lookup"><span data-stu-id="ad495-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad495-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="ad495-111">Remarks</span></span>

<span data-ttu-id="ad495-112">Чтобы получить ссылку на ячейку LockCrop по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ad495-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad495-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ad495-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ad495-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="ad495-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="ad495-115">Для получения ссылки на ячейки LockCrop по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ad495-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad495-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ad495-116">Section index:</span></span>  <br/> |<span data-ttu-id="ad495-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad495-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ad495-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ad495-118">Row index:</span></span>  <br/> |<span data-ttu-id="ad495-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ad495-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ad495-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ad495-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ad495-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="ad495-121">**visLockCrop**</span></span> <br/> |
   

