---
title: Ячейка LockWidth (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Блокирует ширину фигуры таким образом, чтобы его ширина не изменяется при изменении размеров фигуры.
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814162"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="c0462-103">Ячейка LockWidth (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="c0462-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="c0462-104">Блокирует ширину фигуры таким образом, чтобы его ширина не изменяется при изменении размеров фигуры.</span><span class="sxs-lookup"><span data-stu-id="c0462-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="c0462-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c0462-105">**Value**</span></span>|<span data-ttu-id="c0462-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0462-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c0462-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0462-107">TRUE</span></span>  <br/> | <span data-ttu-id="c0462-108">Ширина блокировки.</span><span class="sxs-lookup"><span data-stu-id="c0462-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="c0462-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0462-109">FALSE</span></span>  <br/> | <span data-ttu-id="c0462-110">Ширина не блокируется.</span><span class="sxs-lookup"><span data-stu-id="c0462-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0462-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0462-111">Remarks</span></span>

<span data-ttu-id="c0462-112">Чтобы получить ссылку на ячейку LockWidth по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c0462-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0462-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c0462-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c0462-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="c0462-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="c0462-115">Для получения ссылки на ячейки LockWidth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c0462-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0462-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c0462-116">Section index:</span></span>  <br/> |<span data-ttu-id="c0462-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0462-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0462-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c0462-118">Row index:</span></span>  <br/> |<span data-ttu-id="c0462-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c0462-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c0462-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0462-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c0462-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="c0462-121">**visLockWidth**</span></span> <br/> |
   

