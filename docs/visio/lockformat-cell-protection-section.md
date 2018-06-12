---
title: Ячейка LockFormat (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Блокирует форматирование фигуры, поэтому его нельзя изменить.
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814130"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="68bff-103">Ячейка LockFormat (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="68bff-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="68bff-104">Блокирует форматирование фигуры, поэтому его нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="68bff-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="68bff-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68bff-105">**Value**</span></span>|<span data-ttu-id="68bff-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68bff-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="68bff-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="68bff-107">TRUE</span></span>  <br/> | <span data-ttu-id="68bff-108">Форматирование нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="68bff-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="68bff-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="68bff-109">FALSE</span></span>  <br/> | <span data-ttu-id="68bff-110">Форматирование можно изменить.</span><span class="sxs-lookup"><span data-stu-id="68bff-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68bff-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="68bff-111">Remarks</span></span>

<span data-ttu-id="68bff-112">Чтобы получить ссылку на ячейку LockFormat по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="68bff-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68bff-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="68bff-113">Cell name:</span></span>  <br/> | <span data-ttu-id="68bff-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="68bff-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="68bff-115">Для получения ссылки на ячейки LockFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="68bff-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68bff-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="68bff-116">Section index:</span></span>  <br/> |<span data-ttu-id="68bff-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68bff-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="68bff-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="68bff-118">Row index:</span></span>  <br/> |<span data-ttu-id="68bff-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="68bff-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="68bff-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="68bff-120">Cell index:</span></span>  <br/> |<span data-ttu-id="68bff-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="68bff-121">**visLockFormat**</span></span> <br/> |
   

